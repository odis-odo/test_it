



### df (disk free) and du (disk usage) commands




  Using the -h option with the df command will make file size human readable:

	df -h



  Using the -T option will show the type of filesyte for the mounted storage:

	df -T


  The -x option will exclude a filesystem from the output:

	df -x tmpfs


  Using df with the watch command:

	watch df -hTx tmpfs

  This will run the command every 2 seconds and will show any changes that occur
  such when a filesystem is mounted.




  -----------------------------------------------------




  Basic usage of the du command:

	du /home/odis

  This can be used with any directory or path.



   The -h option makes the filesize human readable:

	du -h



   The --max-depth option will control how deep the du command will go in in the 
   directory:

	du -h --max-depth 1

   The number indicates how many directories deep it will go.




   The -s option will give a summary of the total space used in a directory:

	du -hs



   To view multiple directories make sure to type sudo to minimize any errors:

	sudo du -hs /home/odis /etc



   The -c option will combine the totals of the directories listed:

	sudo du -hsc /home/odis /etc



   To view the summary of all of the subdirectories use the *:

	sudo du -hsc /home/odis/*


    

  

  
