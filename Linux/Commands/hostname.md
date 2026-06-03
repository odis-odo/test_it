
<br>
basic usage just type

~~~
hostname -> this will display the name of the computer
~~~

hostname is stored in /etc/hostname and view the hostname there as well.

 /etc/hosts will have host names for localhost as well for server.

<br>
the -A will alias for the hostname 

~~~
hostname -A
~~~

<br>
the -i will show your local host ip address, the uppercase -I will give ip address that is
associated with the ip address on the network,

~~~
hostname -I
~~~


if you have systemd for your init for your distro you can use the
hostnamectl command.

<br>

to change the hostname of your device use the following:
~~~
sudo hostnamectl set-hostname "Name your changing it to"
~~~










