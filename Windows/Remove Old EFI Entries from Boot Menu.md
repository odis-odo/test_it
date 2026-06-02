
&nbsp;

[Remove Old EFI Entries From Boot Menu](https://www.youtube.com/watch?v=DBCz5p4WY-E)  

&nbsp;

- Run cmd as administrator and at the prompt type `diskpart` 
+ use `list disk`  then to select the disk number using `select disk`
- use `list part` to list the partitions on the disk then `select part 1` for your partition
+ type `assign letter=N` then `exit`  

&nbsp;

- type `N:` to navigate to the directory
+ then `cd efi`  after use `dir` to list the directories inside the efi directory
- remove unwanted directories using `rmdir /s` then the directory name  

&nbsp;

- when done head back into `diskpart` and select the system partition `sel part 1`
+ to remove the letter assigned earlier type `remove letter=N`
- then `exit` when done




