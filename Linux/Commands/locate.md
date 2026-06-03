<br>

basic usage
~~~
locate filename.txt
~~~
run (sudo)updatedb to update files to run accurate results or else it wont find it.

<br>

to run as case insenitive use the -i so wont matter the case.

~~~
locate -i FILENAME.txt
~~~

<br>

use globbing (*) to find files that meet a particualr criteria.

~~~
locate *.txt
~~~

<br>

the -n option allows you to limit by a certain number of lines.
but wont work if it plocate

~~~
locate -n 4 
~~~

<br>

the -c option will show the number of files it found without showing the names of the files.

~~~
locate -c *.txt
~~~

