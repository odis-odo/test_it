
The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)

Use the next level login:
~~~
ssh -p 2220 bandit12@bandit.labs.overthewire.org
~~~

password: 
```
7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```

  <br>

We will first start by creating a directory in /tmp (/tmp/odis) and copy **data.txt** to it.

Using the `xxd` command which can make a hex dump or reverse it back to binary and with the `-reverse` option will do just that:

```
xxd -reverse data.txt
```

Then make a new file with the reversed data redirecting it in this case just call it  "something":

```
xxd -reverse data.txt > something
```

Then use the `file` command to determine what type of file it is:

```
file something
```

This will show the following ouput which happens to be gzipped:

`something: gzip compressed data, was "data2.bin", last modified: Thu Sep 19 07:08:15 2024, max compression, from Unix, original size modulo 2^32 574`

To unzip the gzip file  use the command `gunzip` but first make sure that the file has the proper extension to do that we will use the `mv` command to rename the file with the extension:

```
mv something something.gz
```

<br>

Then it can be unzipped with `gunzip`:

```
gunzip somehting.gz
```

<br>

Which give the uncompressed file `something` and using the `file` command again we get the following output:

`something: bzip2 compressed data, block size = 900k`

<br>

It is a bzip2 compressed file so using command `bunzip2`:

```
bunzip2 something
```

Which gives the following output:

`bunzip2: Can't guess original name for something -- using something.out`

It did not know what the file name was originally so it gave it  `.out`  extension and again using the `file` command to determine the  type of file it is.

```
file  something.out
```

<br>

It gives the following output:

`something.out: gzip compressed data, was "data4.bin", last modified: Thu Sep 19 07:08:15 2024, max compression, from Unix, original size modulo 2^32 20480`

It is again another gzip compressed file so we need to rename it with the .gz extension once more using the `mv` command from earlier.

<br>

After renaming the file we once again use the `gunzip` command to unzip the compressed file 
which gives the following output:

`something: POSIX tar archive (GNU)`

It is a tar archive file  which can be extracted using the `tar` and using the `x` option for extract and the `f` option for force.

```
tar xf something
```

<br>

Using the `file` command on the extracted file `data5.bin` it gives the output `data5.bin: POSIX tar archive (GNU)` so once again we will use the `tar` command for extraction. This time addingthe `v` option for verbose as well.

```
tar xvf data5.bin
```

Which extracts the file `data6.bin` and with the `file` command it outputs that it is a another bzip2 file ,`data6.bin: bzip2 compressed data, block size = 900k`

<br>

Once again `bunzip2` the file which gives the output:

`bunzip2: Can't guess original name for data6.bin -- using data6.bin.out` 

Then with `file` we get the output: `data6.bin.out: POSIX tar archive (GNU)`

Then with `tar xvf` the extracted file is `data8.bin`

Then with `file` the output  is :

`data8.bin:     gzip compressed data, was "data9.bin", last modified: Thu Sep 19 07:08:15 2024`

<br>

Rename the file `data8.bin.gz` and once again `gunzip` the `data8.bin.gz` .

The `file` command shows that the extracted file `data8.bin` is `data8.bin:  ASCII text`

Then just `cat` the file which gives the result :

`The password is FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn`



<br>


The password for the next level (level 13) is :

```
FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
```






