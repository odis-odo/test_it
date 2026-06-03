
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.


Use the next level login:
~~~
ssh -p 2220 bandit9@bandit.labs.overthewire.org
~~~

password: 
```
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
```

  <br>

Using the `strings` command  will filter out any strings(human readable)
content of the file by piping it into `grep` and adding the `=` :

```
strings data.txt | grep =
```

From the output we get the line which contains `D9========== FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey`


<br>


The password for the next level (level 10) is :

```
FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
```






