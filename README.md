# school21_roger-skyline-1
## installation
Get relevant iso from official page.
Find literally any tutorial "how install arch linux on virtualbox". Do it until partitioning.
![this set up was not in my tutorial](./src/00001.png)
## partition
With the commands fdisk -l or lsblk we discover that our harddisk is named /dev/sda.
`lsblk lists information about all available or the specified block
       devices.  The lsblk command reads the sysfs filesystem and udev db to
       gather information. If the udev db is not available or lsblk is
       compiled without udev support than it tries to read LABELs, UUIDs and
       filesystem types from the block device. In this case root permissions
       are necessary.`

You can use fdisk, gdisk or parted. cfdisk is more or less graphical partitioning tool. cfdisk didn't work for me, so I used fdisk:
```
fdisk /dev/sda
```
fdisk commands:
![fdisk ui](./src/00002.png)
View full table: `p`
I created second partition of same type just because, whatever. So, my final table looks this way:
![last fdisk command p](./src/00003.png)
Next we write partition table and exit:
```
w
q
```
hm, looks like I've ruined everything at this point
## update packages