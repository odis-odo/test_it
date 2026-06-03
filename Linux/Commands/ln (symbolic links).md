<br>

### ln (1)               - make links between files

<br>

  To create a link to an other file or directory use  ln followed by the option -s:

	ln -s /home/jay/Documents/Weekly_Report.txt /home/jay/Desktop/

  You type the file that is to be linked with the full path and then the full path of the
  target directory.

  Not adding a the -s creates a hardlink which is just a duplicate of the original file
  and shares the same inode number. You would not be able to move it to another file 
  system which would not point to the file.

  A symbolic is a different inode number which you could move wherever you like and would
  work just the same.

  To find the inode number use the -i option with ls.
