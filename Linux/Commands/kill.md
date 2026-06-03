
<br>
### kill - send a signal to a process

<br>

  Basic usage is as follows:

	kill -9 45622

  The -9 is the signal used to kill the process and the following number is the process
  to kill.
  Can use the pidof command and the name of the application to find it pid number as well
  as using the ps command.

<br>

  The kill command can also be used to kill multiple pids  at the same time:

	kill -9 13484 74212 10234

<br>

  To kill a command using the name you can use the killall command:

	killall -9 nomacs

<br>

  To use a signal by its name you can use the -s option:

	kill -s SIGKILL 12345



  	
