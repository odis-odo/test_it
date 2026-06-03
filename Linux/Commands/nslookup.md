
<br>


### nslookup (1)         - query Internet name servers interactively

<br>

  Basic usage of the nslookup is as follows:

	nslookup learnlinux.tv

<br>

  To lookup a subdomain is as follows:

	nslookup community.learnlinux.tv

<br>

  To lookup the mail records:

	nslookup -query=mx learnlinux.tv

<br>

  To lookup text records:

	nslookup -query=txt learnlinux.tv

<br>

  To find a name server for a domain:

	nslookup -query=ns learnlinux.tv

<br>

  Using a different name server for queries:

	nslookup learnlinux.tv 8.8.8.8 (google)



  

