# CMD

Using  `dir` with the `/r` option will show the stream of a file or files in the current directory 

```cmd
dir /r 
```  

Some of the file names are repeated with a colon on the file name and these are the the alternate data streams for example:  

`MX-25.1_KDE_x64.iso.torrent`    
`MX-25.1_KDE_x64.iso.torrent:Zone.Identifier:$DATA`  

The `$DATA` is just the stream with a data attribute in the Master file table the real name is `Zone.Identifier`.  

To view the file using the `more` command with `<` to redirect the file into the command.  

```cmd
more < MX-25.1_KDE_x64.iso.torrent:Zone.Identifier
```  

This will give information such zone id and what url is was downloaded from:  

`[ZoneTransfer]`  
`ZoneId=3`  
`HostUrl=https://mxlinux.org/`  

<br> 

The different zones are as follows:  

- 0 - Local Machine
- 1 - Local Intranet
- 2 - Trusted sites
- 3 - Internet
- 4 - Restricted sites  

The `Referrer Url` is the webpage where the download was initiated.  
The `HostUrl` is the source of the actual download.  

<br>

### Creating a Stream


To create a stream to  a file using  `echo`:  

```cmd
echo just some text lol > MX-25.1_KDE_x64.iso.torrent:f1
```  

This will echo the text into the strem `f1` and make sure to add the `:` when adding the stream. 

<br> 

Notepad can be used as well: 

```cmd
notepad  MX-25.1_KDE_x64.iso.torrent:checkit
```  

This will create a new stream `checkit` with notepad and can also be opened with it as well.


<br>

To add other types of date such as binaires or files use the `type` command.  

```cmd
type BadApp.zip > MX-25.1_KDE_x64.iso.torrent:bad
```  

Folders can also have data streams add in this way.

<br>

To extract a file from the stream use the `expand` command:

```cmd
expand MX-25.1_KDE_x64.iso.torrent:bad BadApp.zip
```  

This will extract the file under the file name specicfied and does not delete the file in the stream just makes a copy of it.  

The only streams can be removed is if its copied to a different files system like `exfat` or sent through email. If it is copied between other ntfs files systems it will retain the data.  






