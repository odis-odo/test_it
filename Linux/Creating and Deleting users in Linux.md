
### Useradd  - create a new user or update default new user information

To create a new user with `useradd` is as follows:  


```
sudo  useradd -d /home/username -m -s /bin/bash -G sudo,adm "username"

```  

<br>

- The `-d` specifies the  home directory
- The `-m `  will create the home directory so the 
- The `-s` option will specify the default shell of the user
- The `-G` will add the user supplementary groups such as `sudo,adm` etc
- Then follow up with  the name of the user being created. 

<br> 

After creating a the new user it wil require a pass word to log in which can be done with:  

```
sudo passwd "username"

```  

This will then prompt for a password to enter. 

<br> 

### Userdel  - delete a user account and related files

To delete a user from the system use the following:  

```
sudo userdel -rf "username"  

``` 

<br> 

- The `-r` will remove the user come home directory and any files or folders inside it recursively
- The `f`  will force removal of all files