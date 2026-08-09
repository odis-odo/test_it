

### Formating drive for use with Windows and Linux

- To find the drive to format use `lsblk` to list devices or `fdisk -l` to make sure to target the right drive.  


1. Install exfat utilities for linux:  

```
sudo apt update && sudo apt install exfat-fuse

```   

<br> 

2. Use fdisk to partition the drive selected:  


```
sudo fdisk /dev/sdb

```  


<br> 

3. Create a new partition table and clear all the current partition data. Type `o` at the prompt for a `MBR partiton table` or `g` for a `GUID Partition Table (GPT)`.  

<br>

4. Create a new partition type `n` and it will ask you for some values just press enter for default values. 

<br>

5. By default it will give the partion type of `Linux` to change it to `exfat` use the command `t` and fdisk will ask for a number. Choose number `7` for `HPFS/NTFS/exfat` you can see all the available flags by typing `L`).  

<br>

6. Then save the partition table information and write the settings to drive by typing `w` in fdisk.  

<br> 

7. To create the filesytem itself since it does not have one yet use the command:  

```
sudo mkfs.exfat -n "label" /dev/sdb1

```   

The `-n` option  will give the drive a name or you can label in a seperate command `exfatlabel`  


<br>  

If the drive doesnt show up in Windows under `This PC` you may need to set a drive letter in Windows and then it should be visible.


