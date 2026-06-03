<br>

to check scan multiple ips use a dash to a specific number:
~~~
nmap 192.168.2.10-15
~~~

<br>

to use verbose type -v
~~~
nmap -v 192.168.2.10
~~~

<br>

to view service and version information use -sV
~~~
nmap -sV 192.168.2.10
~~~

<br>

to view operating system an ip is running use -A
~~~
nmap -A 192.168.2.10
~~~

<br>

to scan an entrie network just add the subnet identifier(cidr)
~~~
nmap 192.168.2.10/24
~~~

<br>

to view condensed output use -sP
~~~
nmap -sP 192.168.2.10
~~~

<br>

to speed up the scan use the -T5 option
~~~
nmap -T5 192.168.2.10-15
~~~

T5 is a timing template which is the fastest they range from 0-5 T3 is the default, the
 lower the number the slower it goes to if can bypassf being detected
 by IDS (Intrusion defense system).


