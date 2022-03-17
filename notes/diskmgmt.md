# Disk Management

## Partitions
>
* Disk can be divided into parts called partitions.
* Partitions allow you to separate data.
* based on your requirment, you can create paritions.
    Ex:
        1)OS 2) Applications 3)Data

## Partition Tables

### MBR(Master Boot Record)
>
* In the MBR scheme with 32-bit entries, we can only have a maximum disk size of 2 TB
* only four primary partitions are allowed.
* we can use an extended partition that is further divided into logical partitions to overcome this     limitation.
* contains a boot loader that is written in the initial sectors of the drive
* MBR is an old standard compared to GPT

### GPT(GUID Partition Table)
>
* doesn’t contain a boot loader and can have up to 128 partitions
* supports upto 9.4ZB disk sizes
* not supported on older OS

>
    Ex:-
         $> gdisk -l - to verify what type of partition table

### BIOS(Basic Input Output System) and UEFI(Unified Extensible Firmware Interface)
>
* BIOS (Basic Input Output System) is low-level software that performs hardware initialization and loads the boot loader from the MBR. BIOS is being replaced by UEFI.
* Instead of loading a boot loader from the MBR, UEFI uses efi images from the EFI System Partition. With UEFI and GPT, we can have large disk support.

## Mount Points
>
* all partitions are attached to the system via a mount point
* all partitions are connected through the root partition. (/)
* a directory used to access the data on a partition
* /home
    /home/kittu is on partition mounted on /home

----

## LAB

----

>

* fdisk tool to create/modify partitions

Ex:
    $> fdisk -l   -  to display list of devices
    $> fdisk <<disk_name>> -  to create partitions
            -> n - add a new partition (MBR)
            -> w - write partition
            -> g -> gpt partition table

## Disk Management

>
* mkfs -t TYPE DEVICE   -  to create file system
    
    Ex:-
         mkfs -t ext3 /dev/sdb2

         mkfs -t ext4 /dev/sdb3
         mkfs.ext4 /dev/sdb3

* ls -l /sbin/mkfs* -  to list options to specific file systems


## Mounting with mount
>

* mount DEVICE MOUNT_POINT
     
     Ex:-
          mount /dev/sdb3 /opt

