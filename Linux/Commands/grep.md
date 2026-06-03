


### grep, egrep, fgrep, rgrep - print lines that match patterns


<br>

Usng grep to find a particular  word of pattern:
~~~
  cat /etc/ssh/ssh_config | grep Port
~~~

<br>
using the -v option will exclude every line that containss the term:

~~~
cat /etc/ssh/ssh_config | grep -v Port
~~~


<br>
 grep can also be used by itself without having to piped from another command:

~~~
grep Port  /etc/ssh/ssh_config 
~~~


 <br>
 the -n option will show the line number of the search term:  

~~~
grep -n Port  /etc/ssh/ssh_config 
~~~


<br>
the -c option will show the number of times the search term shows up in the file:

~~~
grep -c Port  /etc/ssh/ssh_config 
~~~



<br>
  the -i option will make the earch case insensitive:

~~~
grep -i port  /etc/ssh/ssh_config 
~~~
 
<br>
  to look though all the files in a durectory use the * :

~~~
grep gedit *
~~~


<br>
  the -r option will look though all files and directories:

~~~
grep -r gedit git/personal/anisible/roles/
~~~ 









  
