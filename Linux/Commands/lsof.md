<br>

### lsof - list open files

<br>

  Basic usage of the command:

	lsof

<br>

  Using the wc with -l will give the number of lines:
  
	lsof | wc -l

  Using sudo will show more files than without.

<br>

  TO limit outout to just the user use the -u option then user name:

	lsof -u odis

  Should also use sudo to see all the files.

<br>

  Use the -c option to view files for a specific process:

	sudo lsof -c firefox

<br>

  Use the -p option to show files by process id:

	sudo lsof -p process number

<br>

  To exclude a user type ^ infront of there name:

	 sudo  lsof -u ^odis

<br>

  To list with ip address uss the -i option:

	sudo lsof -i 4 (directory you want to list)

  The 4 is for ipv4 and a 6 would be for ipv6





  
