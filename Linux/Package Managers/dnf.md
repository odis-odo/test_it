

# DNF - Dandified YUM


- Upgrading installed packages to the newest verisons:  

```
sudo dnf [up|upgrade]
``` 
<br>

- Search for packages with keywords:  

```
dnf [se|search] keyword1 keyword2 ...
```  

<br>

- Display inforamtion about a package:  

```
dnf [if|info] package
```  

<br>

- Install new packages (use `--assumeyes` to confirm all prompts automatically):  


```
sudo dnf [in|install] package1 package2 ...
```  

<br>

- Remove packages:  

```
sudo dnf [rm|remove] package1 package2 ...
```  

<br>

- List installed packages:  

```
dnf [ls|list] --installed
```  

<br>

- Find which packages provide a given command:  

```
dnf provides command  

```  

<br>

- Clean cached data

```
sudo dnf clean all|dbcache|expire-cache|metadata|packages
```  
<br> 

<u>Links</u>  

[dnf-tldr](https://tldr.inbrowser.app/pages/linux/dnf)  
[dnf5-readthedocs](https://dnf5.readthedocs.io/en/latest/commands/index.html)  
[Linux Crash Course - The dnf Command](https://www.youtube.com/watch?v=mL1hMBYP1bQ)


