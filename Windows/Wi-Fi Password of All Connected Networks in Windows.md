
### Locating Saved Wireless Passwords in Windows

To locate saved passwords in the command line is as follows:  

```cmd
netsh wlan show profile 
```  

It will show all the Wi-Fi profiles the computer has connected to.

 <br>

 To view the password  use the following command:

 ```cmd
 netsh wlan show profile profile-name  key=clear
 ```  

 The password will be  under `Key Content`

<br> 

 To remove a network use the following command:  

```cmd 
netsh wlan delete profile name="ProfileName"
```


