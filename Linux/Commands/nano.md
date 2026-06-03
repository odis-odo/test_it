<br>

### Nano's ANOther editor, inspired by Pico

<br>

To open a file at a specific line add + then the line number"

~~~
nano +7 file.txt
~~~

<br>

To open a file in read only mode use the -v option:
~~~
nano-v file.txt
~~~

<br>

To go to a specifc line after opening a file press ctl+w and then you will be presented with more options.  One of the options is *Go to Line* which can be used by holding crtl+t and then entering the line number.

<br>

Nano can also do spellchecking with the spell package which needs to installed seperately:
~~~
sudo apt install spell
~~~
After installing when in nano first use ctrl+t and you will get additonal options with spellcheck to use it just use ctrl+s and it will show the correct spelling. To exit just use ctrl+x .