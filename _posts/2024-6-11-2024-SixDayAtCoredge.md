---
 layout: post
 title: DAY SIX AT COREDGE
 date: 2024-6-11
---
**2024-6-11- AS A LINUX ADMIN**

On day six  i have covered some topics from linux which was very important and 
that is Boot processs and linux filesystem which helps me alot. and also i have
covered about Docker. I known about docker's features and functionality...

**Boot Process in linux**

When we click the power button of our system, several processes are executing in the background. It's very 
important to understand the booting process to learn the working of an operating system. It's a must to 
understand how the Linux kernel boots to resolve the booting error. It is a very curious topic to know, 
so let's begin with the basics.

**BIOS**

BIOS is an acronym for Basic Input/Output System. In other words, the BIOS can load and run the MBR 
(Master Boot Record) boot loader. When we first turn on our system, the BIOS first implements a few integrity 
checks of the SSD or HDD.After that, the BIOS finds, loads, and runs the boot loader function, which can be 
detected in the MBR. Sometimes, the MBR is on a CD-ROM or USB stick, like with a live Linux installation. Then, the boot loader function is loaded into memory, and BIOS provides system control to it once it is detected.

**MBR**

MBR is an acronym for Master Boot Record and is liable to load and run the GRUB boot loader. MBR is placed 
in the first bootable disk sector, which is generally /dev/sda, relying on our hardware. Also, the MBR 
includes details of GRUB, or LILO is an older system.

**GRUB**

GRUB is sometimes known as GNU GRUB, which stands for GNU GRand Unified Bootloader. It is the classic 
bootloader for almost all the latest Linux systems. The splash screen of GRUB is often the initial thing we see when we boot our system. It contains a general menu where we can choose some portions.
We can use our keyboard to choose the one we wish our system to initiate with if we have multiple installed
kernel images. The latest kernel image is chosen by default. The splash screen will delay for some seconds 
for us to choose options. It will load the kernel image (default) if we don't. In several systems, we can see 
the GRUB configuration file at /etc/grub/conf or /boot/grub/grub.conf.

**Kernel**

Often, the kernel is called the code of an operating system. It contained full control on everything in our 
system. In this boot process stage, the kernel mounts the base file system that was chosen that is set up in 
the file, i.e., grub.conf. Then, it runs the /sbin/init function, which is always the initial function to be 
run. We can confirm it with its PID (process id), which should be always 1. Then, the kernel creates a 
temporary base file system with the help of initrd (Initial RAM Disk) until the actual file system is mounted.

**Init**

At this stage, our system runs runlevel programs. It would find an init file, generally detected at 
/etc/inittab, to determine the run level of Linux. Modern Linux systems utilize systemd to select a 
run level rather. Then, systemd will start running runlevel programs.

**There are six run labels in the Linux operating system:**

init1 - single user mode 
init2 - multiuser, without NFS
init3 - Full multiuser mode
init4 -
init5 - GUI
init6 - reboot

**LINUX FILE SYSTEM**

A Linux file system is a structured collection of files on a disk drive or a partition. A partition is a 
segment of memory and contains some specific data. In our machine, there can be various partitions of the 
memory. Generally, every partition contains a file system.
The general-purpose computer system needs to store data systematically so that we can easily access the 
files in less time. It stores the data on hard disks (HDD) or some equivalent storage type.

**The below table gives a very short standard, defined, and well-known top-level Linux directory list and 
their purposes:**

**/ (root filesystem):**
It is the top-level filesystem directory. It must include every file needed to boot the Linux system before 
another filesystem is mounted. Every other filesystem is mounted on a well-defined and standard mount point 
because of the root filesystem directories after the system is started.

**/boot:** It includes the static kernel and bootloader configuration and executable files needed to start a 
Linux computer.

**/bin:** This directory includes user executable files.

**/dev:** It includes the device file for all hardware devices connected to the system. These aren't device drivers; instead, they are files that indicate all devices on the system and provide access to these devices.

**/etc:** It includes the local system configuration files for the host system.

**/lib:** It includes shared library files that are needed to start the system.

**/home:** The home directory storage is available for user files. All users have a subdirectory inside /home.

**/mnt:** It is a temporary mount point for basic filesystems that can be used at the time when the 
administrator is working or repairing a filesystem.

**/media:** A place for mounting external removable media devices like USB thumb drives that might be linked to the host.

**/opt:** It contains optional files like vendor supplied application programs that must be placed here.

**/root:** It's the home directory for a root user. Keep in mind that it's not the '/' (root) file system.

**/tmp:** It is a temporary directory used by the OS and several programs for storing temporary files. Also, users may temporarily store files here. Remember that files may be removed without prior notice at any time in this directory.

**/sbin:** These are system binary files. They are executables utilized for system administration.

**/usr:** They are read-only and shareable files, including executable libraries and binaries, man files, and several documentation types.

**/var:** Here, variable data files are saved. It can contain things such as MySQL, log files, other database files, email 
inboxes, web server data files, and much more.

**Types of Linux File System**

When we install the Linux operating system, Linux offers many file systems such as Ext, Ext2, Ext3, Ext4, JFS, ReiserFS, XFS, 
btrfs, and swap.

**Ext, Ext2, Ext3 and Ext4 file system**

The file system Ext stands for Extended File System. It was primarily developed for MINIX OS. The Ext file system is an older 
version, and is no longer used due to some limitations.

**Ext2:**is the first Linux file system that allows managing two terabytes of data. **Ext3:** is developed through Ext2 it is an upgraded version of Ext2 and contains backward compatibility. The major drawback of Ext3 is that it does not support servers because this file system does not support file recovery and disk snapshot.

**Ext4:** file system is the faster file system among all the Ext file systems. It is a very compatible option for the SSD 
(solid-state drive) disks, and it is the default file system in Linux distribution.

**XFS File System**
XFS file system was considered as high-speed JFS, which is developed for parallel I/O processing. NASA still using this file 
system with its high storage server (300+ Terabyte server).


**Btrfs File System**
Btrfs stands for the B tree file system. It is used for fault tolerance, repair system, fun administration, extensive storage 
configuration, and more. It is not a good suit for the production system.

**Swap File System**
The swap file system is used for memory paging in Linux operating system during the system hibernation. A system that never 
goes in hibernate state is required to have swap space equal to its RAM size.
