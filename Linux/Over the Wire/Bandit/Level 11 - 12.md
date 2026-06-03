
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

Use the next level login:
~~~
ssh -p 2220 bandit11@bandit.labs.overthewire.org
~~~

password: 
```
dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
```

  <br>

To decode this rot13 cipher we use vim text editor by opening the file in vim and then just typing `ggg?G` to decrypt the file which gives the result from the text editor:

`The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4`


<br>


The password for the next level (level 12) is :

```
7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```






