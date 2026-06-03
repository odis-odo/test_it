
The password for the next level is stored in the file data.txt, which contains base64 encoded data

Use the next level login:
~~~
ssh -p 2220 bandit10@bandit.labs.overthewire.org
~~~

password: 
```
FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
```

  <br>

To decode the data use the `base64` command with the`-d` option for decoding:

```
cat data.txt | base64 -d
```

Which gives us the result `The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr`


<br>


The password for the next level (level 11) is :

```
dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
```






