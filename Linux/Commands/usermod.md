<br>

### usermod (8)          - modify a user account

<br>

  To usermod to add a user to a group is:

	$ sudo usermod -aG admins (user name)

  admins is the name of the group you are adding the user too.

<br>

  You can also add multiple groups at the same time:

	 $ sudo usermod -aG admins,sudo (user name)

  All you have to do is put a comma between the groups you want to add to the user.

<br>

  To move a users home directory to a new home diretory is as follows:

	sudo usermod -d /home/myhome --move-home (user name)

<br>

  To change the name of a user is as follows:

	sudo usermod -l (new username) (current username)

<br>

  To lockout a user use the -L option:

	sudo usermod -L (username)

<br>

  To unlock a user use the -U option:

	sudo usermod -U (username)

<br>

  The -e option wwill set a date for expiration of a user account:

	sudp usermod (username) -e  2021-08-21
  

