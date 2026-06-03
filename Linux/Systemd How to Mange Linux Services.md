### What is systemd?

- It's an  init system
- It manages all the services that run in the background.
- Most important process running (PID 1) 

<br>

### Working with Units

- Units in Systemd are resoures that it's able to manage
- Includes services,timers,mounts,automounts and more.

 
<br>

```bash
 # Checking the status of a service

 systemctl status service-name 
```

 <br>

```bash
 # To start a service

 sudo systemctl start service-name
```

 <br>

```bash
 # To stop a service

 sudo systemctl stop service-name
```

 <br>

```bash
 # To restart a service

 sudo systemctl restart service-name
```

 <br>

```bash
 # To enable a service to start automatically at system boot.

 sudo systemctl enable service-name
```
 <br>

```bash
 # To disable a servie to not start autmatically at system boot.

 sudo systemctl disable service-name
```


 <br>

### Systemd Unit Directories
 
 1. /etc/systemd/system
 2. /run/systemd/system
 3. /lib/systemd/system
 
<br>

```bash
# Reload a service is not a full restart but will reload the configuraton files

sudo systemctl reload service-name
```

<br>

```bash
# To edit a service file 

sudo systemctl edit httpd.service # service file
```

<br>

```bash
# To make systemd apply any changes that have been made to service files

sudo systemctl daemon-reload
```