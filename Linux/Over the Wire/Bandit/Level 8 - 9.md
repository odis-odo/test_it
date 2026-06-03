
The password for the next level is stored in the file **data.txt** and is the only line of  text that occurs only once.


Use the next level login:
~~~
ssh -p 2220 bandit8@bandit.labs.overthewire.org
~~~

password: `dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc`  

  <br>

For this we will use the `sort` command to sort the content of **data.txt** and pipe it into the `uniq` command with the `-u` option to only print unique lines:

```
sort data.txt | uniq -u
```

<br>


The password for the next level (level 9) is :

```
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
```






