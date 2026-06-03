The password is contained in a hidden file in the **inhere** directory.

Use the next level login:
~~~
ssh -p 2220 bandit3@bandit.labs.overthewire.org
~~~

password: `MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx`

Navigate to the directory **inhere**:

~~~
cd inhere
~~~

When inside the directory use the ls command with the -a to list hidden files contained in the directory:

~~~
ls -a
~~~

A file name **.hidden** appears and just cat the file for the password:

~~~
cat .hidden
~~~

The password for the next level (level 4) is :

```
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```


