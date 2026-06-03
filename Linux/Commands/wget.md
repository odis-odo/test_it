<br>

popular and basic use for downloading a file:

	wget https://wordpress.org/latest.zip

<br>

the -O option allows to to save the file as another name:

	wget -O wp.zip  https://wordpress.org/latest.zip

<br>

the -P will redirect the location to download the file to:

	wget -P /home/odis/Downloads https://wordpress.org/latest.zip

<br>

the -c option will resume an interrupted download:

	wget -c  https://wordpress.org/latest.zip

<br>

to use an input create a text file with the download links you want to download
and use the -i option:

	wget -i fetch-list.txt 




