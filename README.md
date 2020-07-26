# school21_roger-skyline-1
## installation
Get relevant iso from official page.
Find literally any tutorial "how install arch linux on virtualbox". Do it until partitioning.
--pic of settings that helped me
## partition
With the commands fdisk -l or lsblk we discover that our harddisk is named /dev/sda.
`lsblk lists information about all available or the specified block
       devices.  The lsblk command reads the sysfs filesystem and udev db to
       gather information. If the udev db is not available or lsblk is
       compiled without udev support than it tries to read LABELs, UUIDs and
       filesystem types from the block device. In this case root permissions
       are necessary.`

`cfdisk`
Then we start cfdisk to partition our harddisk. You can also use fdisk, gdisk or parted. cfdisk is more or less graphical partitioning tool.
We have choosen to install UEFI or EFI so we choose now GPT.

## update packages