## winsat

Using winsat to test read and write speed of drives:  

```
winsat disk -drive  (drive letter) 
```   

Make sure to run it as admisitrator as well.  


## manage-bde

Using manage-bde to check the status of drive encryption:  

```
manage-bde -status 
```   

 This will show the status of all drives currently connected in windows.  

 To look for specific volumes just add the drives letter after status like so:  


```
 manage-bde -status  (drive letter)
```  

 This also needs to be run as administrator.




