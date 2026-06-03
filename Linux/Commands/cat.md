

to view content of files with cat command basic usage is 
~~~
cat filename.txt
~~~  


to concatenate files together 
~~~
cat filename1.txt filename2.txt
~~~  


to create new files on contents of old files
~~~
cat filename1.txt filename2.txt > combined.txt
~~~


to show line numbers use the -n option 
~~~
cat -n filename.txt
~~~


using cat with chaining commands the --color option will highlight what your greping for as it wont do it be default
~~~
cat filename.txt | grep --color cats
~~~



using the cat command in admistrative example
~~~
cat /etc/ssh/sshd_config | grep --color Port
~~~

another example using wc command (word count)
~~~
cat /etc/ssh/sshd_config | wc -l
~~~