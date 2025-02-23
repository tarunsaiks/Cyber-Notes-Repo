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