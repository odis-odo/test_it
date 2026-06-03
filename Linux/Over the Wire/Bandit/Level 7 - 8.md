
The password for the next level is stored in the file **data.txt** next to the word **millionth**


Use the next level login:
~~~
ssh -p 2220 bandit7@bandit.labs.overthewire.org
~~~

password: `morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj`  

  <br>

For this we cat the `data.txt` and pipe it to the `grep` command with the pattern `millionth`:

```
cat data.txt | grep millionth
```

And the result we get us `millionth       dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc`
  


The password for the next level (level 8) is :

```
dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
```






