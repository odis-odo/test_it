<br>

watch command will run the command given every 2 seconds

	watch ls 

this will show any new files in your directory

<br>

use the watch command to view storage

	watch df -h  

this will show your storage and any changes might occur such as creating new files or transfers.

<br>

use the watch command to view memory

	watch free -m 

 this will show your memory in mb when runnin other commands or programs.

<br>

use the -d option to highlight any changes 

	watch -d free -m

<br>

use the -n option to change the repeat interval

	watch -d -n 0.5 free -m

<br>

use the watch command with commands that contain pipes use quotes around it.

	watch 'ls -lh | grep important_file.txt'


