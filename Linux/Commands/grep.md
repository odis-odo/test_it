


### grep, egrep, fgrep, rgrep - print lines that match patterns


<br>

Usng grep to find a particular  word of pattern:
~~~
  cat /etc/ssh/ssh_config | grep Port
~~~

<br>

Using the `-v` option will exclude every line that contains the term:

~~~
cat /etc/ssh/ssh_config | grep -v Port
~~~


<br>
 grep can also be used by itself without having to piped from another command:

~~~
grep Port  /etc/ssh/ssh_config 
~~~


 <br>


 The `-n` option will show the line number of the search term:  

~~~
grep -n Port  /etc/ssh/ssh_config 
~~~


<br>

The  `-c` option will show the number of times the search term shows up in the file:

~~~
grep -c Port  /etc/ssh/ssh_config 
~~~



<br>

The  `-i`  option will make the search case insensitive:

~~~
grep -i port  /etc/ssh/ssh_config 
~~~
 
<br>
 To look though all the files in a directory use the * :

~~~
grep gedit *
~~~


<br>

The  `-r` option will look though all files and directories:

~~~
grep -r gedit git/personal/anisible/roles/
~~~   

<br>  

The  `-e` option allows specifying more the one matching pattern, to specifiy each seperate pattern:  

```
grep -e print -e check   print.py
```  

<br>  

A simple example of using a regular expression in grep search:  

```
grep [tn] print.py
```  

The square brackets indicate the regular expression grep should look for matches that contain either a *t* or *n* character. Without it grep would just search for text that would match the string tn.









  
