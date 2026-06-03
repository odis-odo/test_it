<br>

### sar - Collect, report, or save system activity information.

<br>

  To customize some defaults go you will need to do the following:

	sudo nano /etc/default/sysstat 

 change collecting stats from ENABLED="FALSE" to ENABLED="TRUE"

<br>

  To run sar command will need to use sudo:

	sudo sar -u -f /var/log/sysstat/sa04 

<br>
  
  To make it simpler just run sar -u:

	sar -u

  This will give similar output to the above command.

<br>

  Use the -r option for memory usage:

	sar -r

<br>

  Use the -S option to viwe swap usage:

	sar -S

<br>

  Use the -b option to view input /output:

	sar -b



