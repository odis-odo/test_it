<br>

### columnate lists  

[Video Link](https://www.youtube.com/watch?v=uL7KvRskeog)

The default behavior  will fill the column first before filling the row as follows:  
~~~
cat file.txt | column
~~~

<br>

Using the -x option will fill the rows before the columns:  
~~~
cat file.txt | column -x
~~~

<br>

Using -t option and the -s for the delimeter with quotes"  
~~~
cat /etc/passwd | column -t -s ":"
~~~

<br>

Headers can be added with the -N option:  
~~~
cat /etc/passwd | column -t -s ":" -N USERNAME,PW,UID,GUID,HOME,INTERPRETER
~~~

<br>

The -H option can used to hide a header:  
~~~
cat /etc/passwd | column -t -s ":" -N USERNAME,PW,UID,GUID,HOME,INTERPRETER -H PW
~~~

<br>

To convert out to a json file use the -J option with the -n to name it:  
~~~
cat /etc/passwd | column -t -s ":" -N USERNAME,PW,UID,GUID,COMMENT,HOME,INTERPRETER -J -n passwordfile
~~~



