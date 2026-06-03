


basic usage of the echo command

	echo "Hello World"


can also echo variables

	msg="Hello World"
~~~
echo $msg
~~~

<br>
the -e allows to change the format of the text when you use the echo command      

 \a for audible

~~~
echo -e "\aHello World" 
~~~

\c will truncate anything after the c.

~~~
echo -e  "This is a Linux\c server." 
~~~

\n will put the output on a new line.

~~~
echo -e "This is a Linux\n server."  
~~~

\t will add tabs the output.

~~~
echo -e "This is a Linux\t server."      
~~~


redirecting echo output to a file

	echo "Logfile started: $(date + '%D %T')" > log.txt 



