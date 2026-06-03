


### head and tail command



<br>
  Basic usage of the head command:

	head /var/log/syslog


<br>
  Basic usage of the tail command:

	tail /var/log/syslog

<br>
  The -n option will show a specific number of lines other than the default 10:


	head -n 25 filename.txt


  The same option can be used for the tail command.


  <br> 
  The -f will follow the file such as a log file in real time and is specific to the
  tail command:


	tail -f filename.txt
