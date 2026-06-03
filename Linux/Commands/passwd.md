<br>

basic usage of passwd:

	passwd

the command will default to the current user if no user is specified will only change the
password for the current user.

<br>

to view statistics of your password use the -S option this will require a sudo when
specifiying  a user:

	sudo passwd -S odis

odis P 2024-10-21 0 99999 7 -1

first field is odis 

second field is P or PS means usable password L for locked password

third field is the date of the last password change for the user

fourth field is password age 0 means it can be changed anytime you want anything higher 

the amount of days that must pass before you can chaneg again.

fifth field is how many days before you have to change the password again

sixth field is how many days for remminder before you have to change the passeword.

seventh field is how many the  days the account will be locked put.

<br>

locking the password for a user using the -l option will need sudo:

	sudo passwd -l voltron

<br>

to unlock a user account use the -u option with sudo:

	sudo passwd -u voltron

<br>

to set a an expiry date for a user use the -x option with sudo then the number of days:

	sudo passwd -x 30 voltron

<br>

to make the user password immediately use the -e option:

	sudo passwd -e voltron

<br>

to delete the password altogether use the -d option:

	sudo passwd -d voltron














