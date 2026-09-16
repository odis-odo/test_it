`

# PACMAN - Arch Linux package manager utility

- [S]ynchronize and update all packages:  

```
sudo pacman -Syu
``` 

<br>  


- Install a new package:  

```
sudo pacman -S package
```  

<br> 

- [R]emove a package and its dependencies:  

```
sudo pacman -Rs package
``` 

<br>  


- Search (s) the package database for a regex or keyword:  

```
pacman -Ss "search_pattern"
```  

<br> 

- Search the database for packages containing a specific [F]ile:  

```
pacman -F "file_name"
``` 

- List only the explicitly installed packages and versions:  

```
pacman -Qe
``` 

<br>  

- List orphan packages (installed as dependencies but not actually required by any package):  

```
pacman -Qtdq 
``` 

<br> 

- Empty the entire pacman cache:  

```
sudo pacman -Scc 
``` 

<br> 


<u>Links  

[pacman-tldr](https://tldr.inbrowser.app/pages/linux/pacman)  
[manned-pacman](https://manned.org/pacman.8)  
[arch-wiki](https://wiki.archlinux.org/title/Pacman/Rosetta)  
[Linux Crash Course - The Pacman Command](https://www.youtube.com/watch?v=HD7jJEh4ZaM)
