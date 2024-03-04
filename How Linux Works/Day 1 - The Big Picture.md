# Why is Linux complicated?

There could be a web server communicating with database server using programs which uses shared libraries, This is all managed by operating system using **ABSTRACTION**.

When riding a car we don't think about how a particular bolt holds the motor or seats inside the car, we ignore the minute details and mechanisms of the car. Rather we focus on how to drive and move from A to B.

Similarly dev's use abstraction as a tool when building such complicated operating systems (Agree?? Linus Torvalds?)

Coming from a ex-developer, there are different terms for an abstracted subdivision like packages in python, header files or libraries in C/C++, modules etc.,

## Levels of Abstraction in Linux

3 main levels of abstraction in Linux.

1. Hardware - includes memory, CPU and storage disks (you know, just hardware (don't complicate or over think with cloud.))
2. KERNEL - OG/Core of Operating System. Does many crucial things, hold on.
3. Processes - Programs running managed by Kernel.
	1. User Space
	2. Kernel Space

![Layers and Sub Layers in Linux](Screenshots/1.1-LinuxSystemOrg.png)

### Hardware - Main Memory (RAM, JAI SRI RAM <3)

- Main memory is just a high-speed, volatile storage area which contains 0's and 1's. (Binary data bro, data stored in binary).
- Bit - either 0 or 1.
- Byte - 8 bits
- Main memory is where kernel interacts and instructs CPU to perform operations and share the results or interact with Input/Output.
- The input and output from peripheral devices in a computer system are channeled through main memory, treated as a collection of bits manipulated by the CPU. In computer systems, a "state" refers to the arrangement of these bits, often described abstractly based on the actions or stages of processes rather than their binary representation. (yes, I used ChatGPT definition)
![](Screenshots/OS_overview.jpeg)

### Kernel - heart of linux

We discuss main memory and states because they form the foundation of the kernel's operations. 

The kernel's tasks, includes
- Process Management
- Memory Management
- Device Driver Management
- system call handling

The kernel tasks are all intimately tied to main memory and require meticulous management to ensure efficient resource utilization and process execution.

#### Process Management

start, stop, pause, resume, scheduling and terminating are some of the actions performed on programs that run on memory (process, see now you know process definition is, definitely A grade this time)

