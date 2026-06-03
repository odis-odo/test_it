<br>

### scp — OpenSSH secure file copy

<br>

  To copy a fike from a local machine to a server is a s follows:

	scp filename.txt dev:/home/user/


  The dev portion is the name or can be the ip address of the server then the
  directory where you like to copy the file too.

<br>

  To copy a file from a server to a local machine is as follows:

	scp dev:/home/user/filename.txt /home/user2

<br>

  To execute a one off command in a remote server without logging in:

	ssh (servername/ipaddress) command (ls)

<br>

  To copy directories use the -r option:

	scp -r backups dev:

<br>

  To retain modification times/dates use the -p option:


	scp -p backups dev:

  This can also be used with -r option as well.

<br>

  To change the port of a server that uese a non standard port use the -P:

	scp -P 2222 filename.txt dev:

