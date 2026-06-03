
<br>

###  ip - show / manipulate routing, network devices, interfaces and tunnels


<br>

 the basic go to command:

	ip addr show

or


	ip a


 this will show your network interfaces and there ip address.

<br>

 to show information on a specfic interface:

	ip addr show dev (name of interface)


<br>

to down an interface:


	sudo ip link set eth0 down

<br>

 to reverse the process:

	sudo ip link set eth0 up

<br>
 
  to  add an ip address to an interface:


	  sudo ip addr add 192.168.0.123/24 dev eth0	


<br>
  to remove an ip address from an interface:

	  sudo ip addr del 172.16.250.105/24


***
Routing Commands

<br>
   to the route of an ip address:

	   ip route show


<br>
   to add a route to the routing table:  
   

	sudo ip route add  172.16.252.0/24 via 172.16.250.1 dev eth0


<br>

  to remove a route from a routing table:

    sudo ip route del  172.16.252.0/24 via 172.16.250.1 dev eth0

<br>
 
to show link layer (interface statistics):

	ip -s link show eth0 		

<br>

can also be combined with watch command:

	 watch    ip -s link show eth0


<br>


Bonus Tips

to show the coloured and easier to read:

	ip -c a

<br>

to show just the ip address and coloured output and just the ipv4 address:


	ip -c -br -4 a



 





  	










 
 




