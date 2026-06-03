

basic usage of date command:

	date


the -r command shows the last time  of a file modification:

	date -r /etc/hosts



using the echo command to add a message to the output:

	echo "$(date): Script has finshed."




to format output just showing current month:

	date +%m




to format output just showing current hour in 24 hour time:

	date +%H ( a lower case h will show month in alphabetical form.)



formating date and time with message using subshell in brackets:

	echo "$(date "+%Y-%m-%d %H:%M:%S") - Script has finished."



to set the date and time and need sudo:

	sudo date --set="20240816 14:27"



to find out what day you were born  (Fun Game/Example)

	date +%A -d "1984-02-08"






