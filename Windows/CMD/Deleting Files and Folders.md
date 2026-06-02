
To delete files in with command prompt use the `del` command  followed by the name of the file. If the file is marked as read only use the `/f` flag to force deletion as in the following:

```
del /f file.txt
```

<br>

To  delete folders use either `rmdir`  or `rd` command:

```
rmdir foldername
```

<br>

If the folder contains files or subdirectories use the `/s` flag to delete the folder and its contents:

```
rmdir /s foldername
```

<br>


If you do not want to the prompt asking for confirmation you can use the `/q` flag:

```
rmdir /s /q foldername
```

<br>

You may encounter issues with deleting files due to read only attributes or other permission issues for that use the `/f` with `del` to force deletion.  

It is possible to delete files using a batch file or by adding a custom command to the Windows Explorer menu. As an example create a batch file `delete.bat` with the following:


```
@echo off
cd %1
del /f /q /s *.*
cd..
rmdir /s /q %1
```

Then you can add a registry entry into the context menu to run the batch file.

<br>

If you wanted to delete all the files in a folder without deleting the folder itself is as follows:

```
del /f/q/s *.* 
```

You can also add a `> nul` after the asterisk if you want to hide the output while deleting.



 

