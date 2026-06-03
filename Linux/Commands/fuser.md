### identify processes using files or sockets

[Video LInk](https://www.youtube.com/watch?v=xF8uttDarG0)

<br>

Running the fuser command on a mount point of  drive that cant be ejected:
~~~
fuser /mnt/wslg/distro/
~~~
It will show two numbers and the letter c beside them, the numbers are the process id that is holding up the directory. The letter c is the current mount point being run.
~~~
12041c 12105c
~~~

<br>

Using the -v will give more detailed output: 
~~~
fuser -v  /mnt/wslg/distro/
~~~

<br>

To kill the process holding up the drive you can use the -k option"
~~~
fuser -k /mnt/wslg/distro/
~~~
Sudo may be necessary to see deeper into the processes holding up the drive.

<br>

With external drives use the -m option to pass it through the dev folder:
~~~
sudo fuser -m -v /dev/sda1
~~~

<br>



