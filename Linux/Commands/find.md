


### find - search for files in a directory hierarchy



Basic usage of the find command:

```
find /home/odis -name *.txt
```


  The wildcard  * will return any files with .txt extension also as a side note
  yo may need to put the argument in quotes  ("*.txt").

<br>
  To find something specific:

```
find . -name Documents
```
find . -name Documents

  The . is for your current diectory so this will look for the directory Documents.

<br>
To find a directory or file specifically use the -type option:

```
find . -name Documents -type f
```

  The f after type indicates file and a d would indicate a directory.  

<br> 

Using the `-exec` executes a command based on what `find` finds:  

```
find / -name "*.txt" -exec grep -l "shingots" {} +
```  

- The `grep` command is being run with the `-l` option to show just the file path which contains the pattern =="shingots"==.
- The empty pair of `{}` is place holder for the results of `find`
- The `+` terminates the command and run it only once  

<br> 










