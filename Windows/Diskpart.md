[How to Format Storage Device with Diskpart Utility in Windows](https://www.youtube.com/watch?v=ucMtoFn5bzs&list=PLc6zqGSJMvCRA_qiiEOpiFhaJeilHIyXk&index=32)

<br>

- Diskpart must be run as Administrator to run it jut type `Diskpart` in the command line.  
- The `list disk` command will list all the disks connected to the computer
- use `select disk` then the number of the disk to format.   

<br>

- To clear everything off the disk use the command `clean`
-  Create a partition with the command `create partition primary`
-  Can also be abbreviated with `create part prim`

<br>

- The `list partition` command will list the partition(s) on disk
-  `select partition` to select the partition to format it

<br>

- Using the `format` command to format the partition with a file system.

```
format fs=ntfs label=my_drive quick
```

- The above command will format the drive with a `ntfs` file system, label the drive with  `my_drive` and do a `quick` format.
-  To assign a drive letter if need use the command `assign letter=`






