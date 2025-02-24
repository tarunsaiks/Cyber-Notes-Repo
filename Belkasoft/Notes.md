# Windows File Systems

Bits - 0 or 1
Bytes - 8 bits
Sector - smallest addressable storage unit.
Cluster - aka  allocation unit, a cluster is a group of one or more contiguous sectors.

File system organization - FAT or NTFS
**Partition**: A partition is a low-level division of a physical disk into separate, contiguous regions. It defines specific areas of the disk but does not inherently include a file system.
**Volume**: A volume is a storage area that has been formatted with a file system and is ready for data storage. Essentially, it is what the operating system recognizes as a usable storage area, often assigned a drive letter (like C: or D:) in Windows environments. In Windows, a single partition can contain one volume, but a volume can also span multiple partitions or disks, especially in configurations involving dynamic disks.

## FAT
FAT, or File Allocation Table, was developed in 1977 by Microsoft Corporation. FAT is not used as much on computers these days. However, the majority of flash memory storage is still formatted using the FAT file system. In addition, FAT is also frequently used in electronic devices with miniature hard drives.

versions:  FAT12, FAT16, FAT32, and exFAT.
### Components of FAT

1. Boot Sector - Beginning of volume, contains essential info about file system, and BIOS Parameter Block
2. FAT
3. Root Directory region - located immediately after the FAT region and has a fixed size. It contains directory entries for files and subdirectories, including metadata such as file names, attributes, timestamps, and the starting cluster number. In FAT32, stored in data region.
4. Data region - occupies majority of volume. Divided into clusters, which stores the files and directory data. FAT keeps track of sequence of clusters for each file as files can occupy more than one cluster.

The size of one cluster is specified in the Boot Record and can range from a single sector (512 bytes) to 128 sectors (65536 bytes). The sectors are continuous block, makes cluster continuous blocks of space.

## File storage process

1. When a file is created, the OS searches the FAT for free clusters to allocate to the file.
2. The system creates a directory entry for the file, recording metadata and the starting cluster number.
3. If the file spans multiple clusters, the FAT entries are updated to form a linked list (I still remember data structures. DSA trauma moment), with each entry pointing to the next cluster in the sequence. If the allocated clusters are not contiguous the pointers help to keep track of these clusters.
4. The end of the file is marked with a special end-of-file (EOF) marker in the FAT.

FAT File Metadata
- **Filename**: The name of the file, usually following [the 8.3 filename or SFN convention](https://en.wikipedia.org/wiki/8.3_filename) (up to 8 characters for the name and 3 for the extension).
- **File Attributes**: Flags indicating properties such as read-only, hidden, system file, or directory.
- **Starting Cluster Number**: The index of the first cluster where the file data begins.
- **File Size**: The total size of the file in bytes.
- **Timestamps**: Information regarding creation, last access, and last modification times of the file.