

<br>
  The lsusb command will show usb devices and the basic usage as follows:

	lsusb

<br>
  Using the -t option will display information in a tree view:

	lsusb -t

<br>
  The lspci will display devices on the pci bus:

	lspci

  
<br>
  The lshw will give detailed information on your entire system:


	sudo  lshw


  Use sudo with th ecommand to see all information.

<br>
  Adding the -html option will display as html file and can be redirected to 
  an actually html to view in a browser.


	sudo lshw -html > hwinfo.html


<br>
  To show condensed inforation use the -short option


	sudo lshw -short


<br>
  To show information on cpu use the lscpu command:


	lscpu


<br>
  To show storage devices sue the lsblk command:

	lsblk



  
