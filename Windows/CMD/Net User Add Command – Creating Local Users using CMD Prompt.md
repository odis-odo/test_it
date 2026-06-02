<br>

[Net User Add Command – Creating Local Users using CMD Prompt](https://shellgeek.com/net-user-create-local-user-using-cmd/)  


<br>

The net user syntax to a new user with a password:  

```
net user /add username password
```

Replace [username] with the desired username for the new user and [password] with the password you want to assign.

<br>

To show all users on a local computer use `net user`:

```
C:\Users\Odis> net user
```


<br>

The `/fullname` will provide the full name for a user account:

```
net user odis /fullname:"Odis Odo"
```

<br>

To add a user to a local group use the `net localgroup`  command to a specific groupname:

```
net localgroup administrators odis /add
```

This would add the user to the **administrators** group.

<br>

To **remove** a local user use the `net user username /remove` command :

``` 
net user odis /delete
```


