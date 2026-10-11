

# APT - Advanced Package Tool

- Update the list of available packages and versions:  

```
sudo apt update
```
<br>  

- Search packages by name or description:  

```
apt search package
```  

<br>  

- Search packages by name only (supports wildcards like` *`):  

```
apt list package 

```  

<br> 

- Show detailed information about a package:  

```
apt show package 

```  

<br> 

- Install a package, or update it to the latest version:  

```
sudo apt install package
```  

<br>  

-  Remove a package (use `purge` instead to also remove configuration files):  

```
sudo apt remove package
```  

<br> 

- Upgrade all installed packages to their latest versions:  

```
sudo apt upgrade
```  

<br> 

-  List all installed packages:  

```
apt list [-i|--installed]
``` 

<br> 

<u>Links</u>  

[apt-tldr](https://tldr.inbrowser.app/pages/linux/apt)	  
[maned-apt](https://manned.org/apt.8)  
[Linux Crash Course - The apt Command](https://www.youtube.com/watch?v=1kicKTbK768)

