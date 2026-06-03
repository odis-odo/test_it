<br>

Installing Updates in Ubuntu:

To synchronize package repository an show available upgrades:

	sudo apt update 

<br>

To upgrade available packages:

	sudo apt dist-upgrade

  or

	sudo apt upgrade



The dist-upgrade will upgrade everything at once where as if you just use
the upgrade option by itself it only  update packages that dont require to be 
removed or installed.

<br>
Installing Updates in CentOS:


To synchronize package repository and show available upgrades:


	sudo dnf update


When finished it will ask you if want to update the packages after updating 
and no is th default so press y and then enter.


<br>
Installing Updates on Arch:


To synchronize package repository and show available upgrades:


	pacman -Syyy



To upgrade available packages:


	pacman -Syu









