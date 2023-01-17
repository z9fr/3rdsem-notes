* Everything is a file , files are objects with properties and methods

Four components of UNIX
* Boot block - block is a disk allocation of atleast 512 bytes, contains bootstrap code, UNIX/Linux has only one boot block
* Super block - Indicates disk geometry, available space and location of first inode, manages file systems
* Inode block - First data after superblock
* Data block - where directories and files are stored

Types of linux distributors
* Desktop
* Server or enterprise
* Live CD

# Linux forensics

Utilities for imaging and disk analysis - dd, sfdisk, fdisk, md5sum

Why linux for forensics - 
* Greater control
* Flexibility
* Power

Advantages of linux in forensics - 
* Software availability and accessibility
* Efficiency 
* Optimization
* Support

Disadvantages of linux in forensics - 
* Investigator may need to be specially trained to use linux
* Linux is open source OS, it is frequently updated

# Precautions during investigation

* Do not run programs on compromised system
* Do not run programs that will modify metadata and directories
* Write results of investigation to a remote location
* Calculate hash values of data to avoid alterations

# UNIX and linux boot process

* Intruction code in firmware loaded to RAM ( checks hardware and loads boot program )
* Boot program loads kernal and transfers control to kernal
* Kernal identifies all devices
* Boots system on single user mode
* Run startup scripts
* Changes to multiuser mode
* Identifies root directory
* Sets hostname and time zone
* Runs consistency checks on file systems
* Starts services and set up the NIC
* Establish user and system accounting and quotas

# LiLo ( linux loader ) and GRUB ( Grand Unified Boot Loader )

* LiLo - old boot manager, can start two or more OSs
* GRUB - More powerful than LiLo, command line or meny driven


Any file systems on partitions defined during installation are mounted automatically with each boot

# Data collection

* Forensic investigators use their own toolkit
* Toolkit - nc, dd, datecat, pcat, Hunter.o, insmod, NetstatArproute, dmesg

Steps to collect data
1. Media mounting - mount toolkit to external media, calculate hash value 
2. Collect current date result, presented in UTC format
3. Cache tables - collect Mac address cache table
4. Collect information about current connections and open TCP/UDP ports
5. Acquire physical memory image
6. List modules loaded to kernal memory
7. Collect information about all processes 
8. Collect suspicious processes
9. Collect info about compromised system
10. Gather info about current time






