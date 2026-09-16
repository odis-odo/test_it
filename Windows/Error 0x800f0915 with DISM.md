
<br>

The error **0x800f0915** occurs when using the `DISM /Online /Cleanup-Image /RestoreHealth` command and it slows down around 60ish % mark then fails.  


## Possible Fixes  

<br> 

### Fix #1 - Clear out the Update Cache  

Try clearing out the windows update cache from the system.  

Use the following commands as **Administrator** in **Command Prompt**.  

```
net stop wuauserv
```  

- This will stop the **Windows Update Service**   

Followed up with:  

```
net stop bits
```  

- This will stop the **Background Intelligent Transfer Service**  


<br> 

Open **File Explorer** and go to `C:\Windows\SoftwareDistribution` then select everything inside it and delete it.  

Back in the Command Prompt run the first two commands again to restart the servicess:  

```
net start wuauserv
net start bits
```  

Run the DISM command again.  


### Fix #2 Reset the Update Engine  

IF the command still fails the signature database maybe corrupt, renaming will force Windows  to build a new one.   

Run the command: 

```
net stop cryptsvc
```  

- This will stop the **Cryptographic Services (cryptSvc)**  

<br>

Then rename the catroot file:  

```
ren C:\Windows\System32\catroot2 catroot2.old
```  

<br> 

Restart the `cryptsvc`:  

```
net start cryptsvc
```  

<br> 

Reset the network stack with:  

```
netsh winsock reset
```  

Restart the PC the winsock reset doesn't take effect until you do.  
Try DISM command again after the reboot and if it goes further than 60ish % this time, you’re on the right track.  


###  Fix #3  Give DISM the Files Manually  

Use the Windows ISO which a single file containing Windows installation files.  

To use first check the build Of windows:  

- Press **Windows + R** , then type **winver** press **Enter**, look for the number after **OS Build** near the top. The ISO you should match or be newer if recently download from Microsoft site. 
-  Right-click the downloaded **.iso** file and choose **mount**.
- Open **This PC** a new drive will appear  usually **D:** or **E:**  

Open command prompt and run the command swapping E: for your drice letter:  

```
DISM /Online /Cleanup-Image /RestoreHealth /Source:WIM:E:\sources\install.wim:1 /LimitAccess
```  

It may look like its frozen around 20% or so just give it time and then look for the 
"The restore operation completed successfully" 

- The `/LimitAccess` option is what stops DISM from using windows update if not used it could break it again.
- The `/Source` option is the path to `install.wim` or `install.esd` in the windows iso file. 
-  Note: if the iso has `install.esd` just switch the `wim` with `esd` in the above command.


### Fix #4 If the ISO Command Fails  


Two things go wrong here, and both have a one-line answer.

The **:1** on the end of that command means “use the first edition in the image.” But an ISO holds several editions — Home, Pro, Education — and index 1 is often Home. If you run Pro, DISM is comparing your files against the wrong version and refusing to continue.  

The command is as follows:  

```
dism /Get-WimInfo /WimFile:E:\sources\install.wim
```  

It will show a list that will show index numbers check for the edition that you have then change the `:1` so whatever number your edition matches.  


The other problem: some ISOs ship an **install.esd** file instead of **install.wim**. Open the **sources** folder on the mounted drive and look. If yours says esd, swap both words in the command — **/Source:ESD:E:\sources\install.esd:1** — and it works the same way.


<br> 


Can also try using the `/StartCompinetCleanup` option which removes outdated component versions and reduces stored update files. 

```
DISM.exe /Online /Cleanup-Image /StartComponentCleanup
```  


###### Links  

[DISM RestoreHealth Failing With 0x800F0915 – Top 7 Fixes](https://thegeekpage.com/dism-restorehealth-failing-with-0x800f0915-top-7-fixes/)









