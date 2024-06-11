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






**BIOS**

BIOS is an acronym for Basic Input/Output System. In other words, the BIOS can load and run the MBR (Master Boot Record) 
boot loader. When we first turn on our system, the BIOS first implements a few integrity checks of the SSD or HDD.
After that, the BIOS finds, loads, and runs the boot loader function, which can be detected in the MBR. Sometimes, 
the MBR is on a CD-ROM or USB stick, like with a live Linux installation. Then, the boot loader function is loaded 
into memory, and BIOS provides system control to it once it is detected.

MBR

MBR is an acronym for Master Boot Record and is liable to load and run the GRUB boot loader. MBR is placed in the first bootable disk sector, which is generally /dev/sda, relying on our hardware. Also, the MBR includes details of GRUB, or LILO is an older system.

GRUB

GRUB is sometimes known as GNU GRUB, which stands for GNU GRand Unified Bootloader. It is the classic bootloader for 
almost all the latest Linux systems. The splash screen of GRUB is often the initial thing we see when we boot our system. 
It contains a general menu where we can choose some portions.
We can use our keyboard to choose the one we wish our system to initiate with if we have multiple installed kernel images. The latest kernel image is chosen by default. The splash screen will delay for some seconds for us to choose options. It will load the kernel image (default) if we don't. In several systems, we can see the GRUB configuration file at /etc/grub/conf or /boot/grub/grub.conf.
Kernel
Often, the kernel is called the code of an operating system. It contained full control on everything in our system. In this boot process stage, the kernel mounts the base file system that was chosen that is set up in the file, i.e., grub.conf. Then, it runs the /sbin/init function, which is always the initial function to be run. We can confirm it with its PID (process id), which should be always 1. Then, the kernel creates a temporary base file system with the help of initrd (Initial RAM Disk) until the actual file system is mounted.
Init
At this stage, our system runs runlevel programs. It would find an init file, generally detected at /etc/inittab, to determine the run level of Linux. Modern Linux systems utilize systemd to select a run level rather. Then, systemd will start running runlevel programs.
There are six run labels in the Linux operating system:
0- halt


