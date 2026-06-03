<br>

To label or relabel a drive in Linux that is exfat use the following command:

``` 
sudo exfatlabel /dev/sdXY "the label name goes here"
```

<br>

exfat-utils needs to be installed to use the command to install it use the following:  

```
sudo apt install exfat-utils
```

<br>

The drive should be unmounted first before labeling/re-labeling to avoid any possible data corruption.

Other command for labeling drives for their respective file systems:

For FAT16 and FAT32 partitions, use mlabel from the `mtools` package.

For NTFS partitions, use ntfslabel from the `ntfs-3g` package.

For ext2, ext3, or ext4 partitions, use `e2label`.

For JFS partitions, use `jfs_tune`.

For ReiserFS (v3) partitions, use `reiserfstune`.

For XFS partitions, use `xfs_admin`



