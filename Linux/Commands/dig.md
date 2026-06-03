



### dig (1)              - DNS lookup utility


  Basic usage of the dig command:
	
	dig learnlinux.tv

  
  To look up a subdomain with dig:

	dig community.learnlinux.tv



  To look up mail exchange (MX) records:

	dig learnlinux.tv MX



  To look up text (TXT) records:

    dig learnlinux.tv TXT



  To look up name server (NS) records:

    dig learnlinux.tv NS




  To look up records with a specfic dns server is a as follows:

    dig @8.8.8.8 learnlinux.tv 




  To view a short version of the output +short:

    dig +short learnlinux.tv 




  To check ttl (time to live) values:

    dig +ttl learnlinux.tv 

