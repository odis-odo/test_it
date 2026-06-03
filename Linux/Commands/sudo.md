<br>

### sudo (8)             - execute a command as another user

<br>

  To find out which sudo group your distribution uses cat the sudoers file:

	(sudo) cat /etc/sudoers

  It should near the bottom for allow if its sudo or could be called wheel.

<br>

  To list the sudo privileges use sudo with the -l option:

	sudo -l

<br>

  To run a previous command with sudo use !!:

	sudo !!

<br>

  To edit the sudoers file you must use the visudo command:

	sudo visudo  
