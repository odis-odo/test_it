
#### WMIC

Open a command prompt and enter the following:

```
WMIC useraccount get name,sid
```

This will output the all the users and their SID on the system.

<br>

#### Regedit

Alternatively a users SID can be found through the registry open regedit and navigating to :

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\ProfileList`

<br>

#### PowerShell

PowerShell can also be used to find the SID  here are a few ways:

1. Using the `System.Security.Principal.NTAccount` class:

```powershell
$name = '[email protected]'
(New-Object System.Security.Principal.NTAccount($name)).Translate([System.Security.Principal.SecurityIdentifier]).value
```

Replace `$name` variable with the user's domain and username.

 &nbsp

2. Using the `Get-ADUser` cmdlet if you have the Active Directory module installed:

```powershell
Get-ADUser -Identity '[email protected]' | Select-Object -ExpandProperty SID
```

Replace the `-Identity`  parameter with the user's domain and username.

 &nbsp

3.  Using the `Get-LocalUser` cmdlet to get the SID of a local user:

```powershell
Get-LocalUser -Name 'username' | Select-Object -ExpandProperty SID
```

Replace 'username' with the name of the local user. 

&nbsp

4. Using the `whoami` command with the /user option:

```
whoami /user
```


***

### Definition of SID

A Security Identifier (SID) is a unique value used in Windows operating systems to identify user accounts, groups, and other security principals. Each SID is created when an account is established and remains constant even if the account name changes, ensuring consistent identification for security purposes.
