
<br>

# Journalctl Utility

To display all logs in linux system use:

```
journalctl
```


To get the help menu use the -h option

```
journalctl -h
```

<br>	

### Log Priorities and Facilities

Here is a list of logging system priorities:

- emerg (0)
- alert (1)
- crit (2)
- err (3)
- warning (4)
- notice (5)
- info (6)
- debug (7)


To view high priority logfiles using the -p option:  

```
journalctl -p "emerg"  
```  

You can also use the priority number as well such as 6 (info) 

```
journalctl -p 6
```  

<br>

### journalctl Queries

journalctl has the ability to query logs such as for events,users, and time that is very similar to human  language. 
If you only wanted to see the events from the last 24 hrs:  


```
journalctl -q --since "24 hours ago"
``` 


This will quietly retieves the last 24 hours of log events the `-q` flag is for "quiet". It suppresses messages that are noisy and may leave traces of your activity.  


You can also search for events by user and the root user in Linux is designated with the ID 1000 so the command will look like so:

```
journalctl _UID=1000 --since "24 hours ago"
```  

To view kernal logs use the `-k` option:  


```
journalctl -k --since "24 hours ago"
```  

<br>	

### Using journalctl to Cover Your Tracks


To cleanup logs you  will need to use `sudo` in the following:

```
sudo journalctl -u apache2 --vacuum-time=1d
```  

This command will delete all the logs associated with the apache2 web server in the past day.  


You can also use the shred command to shred files in the journal directory:

```
shred -f -n 10 /var/log/journal/subdirectory name*.*
```  

The `-f` option will give premission to shred the files and the `-n` option will be the number of times to overwrite.


<br>	

### Disabling Logging

To disable logging use a any text editor with sudo and edit the `journals.conf`:  

```
sudo mousepad /etc/systemd/journald.conf
```  

Look for the line at the end that says `#storage=auto` and change that line to say `storage=null`. Then delete the comment mark (#) before it and save the file and restart journald:  

```
sudo systemctl restart system-journald
```  

This will stop and start journald and when it restarts it will use the new configuration and send all logs to null.



