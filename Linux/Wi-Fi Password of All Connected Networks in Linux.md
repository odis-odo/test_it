
### Locating Saved Wireless Passwords in Linux

To locate saved passwords in the command line is as follows:  

```bash
cd /etc/NetworkManager/system-connections/ 
```  


This directory contains all the profiles of Wi-fi networks that the deivice has connected to.

 <br>

 To see the profiles in directory use `ls` and to view  the contents of the profile  using`cat`  and `sudo`:  

 ```bash
 sudo cat WIFI_SSID_NAME
 ```  

 The password will be  `psk="PASSWORD"`  

<br> 

 To remove a network use the following command:  

 ```bash
 sudo rm /etc/NetworkManager/system-connections/NETWORK_NAME 
 ```


