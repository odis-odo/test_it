# Powershell


To view the files and data streams use the `Get-item` cmdlet with `-Stream` parameter:  
```Powershell
Get-Item * -Stream *
```  

`Get-item *` acts the same way as `dir` in cmd but will not show data streams thats where adding the `-Stream *` will display all the streams in using the `*`.   

<br>

To filter the results to just show `Filename` and `Stream` is as follows:  

```Powershell
Get-Item * -Stream * | select Filename,Stream | where Stream -NotMatch :$DATA
``` 

This will not only display `Filename` and `Stream` but will also filter out `$DATA` stream as well. Most files will have the `$DATA` so you only see files that have streams added to them.  

<br> 

To read the content from a stream use the `Get-Content` with `-Stream` parameter and the stream name.  

```powershell 
Get-Item .\MX-25.1_KDE_x64.iso.torrent | Get-Content -Stream Zone.Identifier
```  

<br> 

### Creating a Stream

To create a stream using the `Set-Content` cmdlet with the `-Stream` parameter:

```Powershell
 Get-Item .\MX-25.1_fluxbox_x64.iso.torrent | Set-Content -Stream lol -value "lol can you see this?"
 ```  

 The `-Stream` parameter is the name of the stream and `-value` is the content of the stream itself.  

 ### Clearing a Stream
 
 Use `Clear-Content` and the stream to clear the contents of a stream:
 
 ```Powershell
Get-Item .\MX-25.1_fluxbox_x64.iso.torrent | Clear-Content -Stream lol
```  

### Removing a Stream

To remove a stream entirely use the `Remove-item` cmdlet plus name of the stream:  

```Powershell
Get-Item .\MX-25.1_fluxbox_x64.iso.torrent | Remove-Item -Stream lol
```   

### Removing a Zone Identifier

To remove the zone identifier using the `Unblock-file` cmdlet to unblock the file:  

```Powershell 
Unblock-File .\MX-25.1_fluxbox_x64.iso.torrent
```



 

 


