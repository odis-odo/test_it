


### diff - compare files line by line



  Basic usage of the diff command:


	diff file1.txt file2.txt 

  You can also use an exit code to confirm they are the same 0 means they are:

	echo $?



  The -s option will give verbose and explicitly say they are the same output:


	diff -s file1.txt file3.txt


  
  If the  diff command shows differences the corresponding symbols will show:


  < the arrow pointing left is for the first file on the left.


the arrow pointing right is for the second file on the left.

  24a25,39 this shows where the difference in the files and the  line number.

  The number 24 refers to the line number for the file on left.

  The number 25,39 refer to the line numbers on the right.

  The a stands for something to be added to nake the files the same.

  If it were a c it means something needs to changed to make them the same.

  If it were d it  mean something a line was deleted.





  Can you use colordiff to colorize the differnces infiles but may need to install 
  if not available.

	colordiff file1.txt file2.txt 



  The -u gives more information but it also eaaier to read if there is any changes:

	diff -u file1.txt file2.txt 
 





   



