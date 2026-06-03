<br>

basic usage

	ss

<br>

use the -t option to show tcp connections specifically.

	ss -t

<br>

use the -l combined with -t option for listening tcp connections

	ss -lt

<br>

use the -u and -a option to see all udp connections

	ss -ua

<br>

use the -lu option for listenng udp connections

	ss -lu

<br>

use the -s option for network statistics

	ss -s



can be combined with watch command which will refresh the list every 2 seconds.
press ctrl + C to cancel it when done.

	watch ss -s

<br>

use the -4 to view ipv4 connections and -6 to view ipv6 connections
~~~
ss -4
~~~
~~~
ss -6
~~~

<br>

to view a specific port use the following just change 22 to whichever port you need

	ss -at '( dport = :22 or sport = :22 )'






