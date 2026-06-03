
The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.

Use the next level login:
~~~
ssh -p 2220 bandit4@bandit.labs.overthewire.org
~~~

password: `2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ`

First thing is to cd into the inhere directory:

`cd inhere`

The password can be found  by  using `cat < -file07` for each file or it can be done by cating them all by doing this:

```
cat ./-file00 ./-file01 ./-file02 ./-file03 ./-file04 ./-file05 ./-file06 ./-file07 ./-file08 ./-file09
```

Which will give you this output and just look for the human readable text>

`�p��&�y�,�(jo�.at�:uf�^���@i�R�,�Λ�:Y���?�%�A����B��ͩ�3�        �)Ʈ�#Y��-6c��IR-�$����:�����/�
                                                                                              ������qGi��,�2�Yb�
dۙ�rOx����h0~ey
��c�~�h�n��G1}���ߓ��ߤ��W>��#lk�d�ܮ��yE��6�0]�\�$�1�%�������o@��b/��4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
�nS�
�<��]�
W��e�˥m�����O��D��2g��?�����`>5HYA�u���8�g�`0�$`��`

<br>

It can also be done by using the `file` command with a wild card which will go through all the folders in the current directory and show the  file type in the output.

```
file ./*
```

<br>

Alternatively the `strings` command can used to the same effect and will only show the files and folders that contain strings.

```
strings ./*
```





The password for the next level (level 5) is :

```
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```






