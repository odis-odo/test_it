
<br>

##### Disable Windows Lock screen direct to Login Prompt

<br>

Go to  `HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows`  

Create new key called `Personalization`  

Create a new DWORD (32-bit) Value called  `NoLockScreen`  

<<<<<<< HEAD
Double click it and set the value to 1   


&nbsp;  


#### Disable Dynamic Search Box  

&nbsp;

Go to `HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\SearchSettings`  

Create a new DWORD (32-bit) Value `IsDynamicSearchBoxEnabled`  

Set the Value to 0 to disable it.  


&nbsp;  

####  Remove Bing From start  

&nbsp; 

Go to `HKEY_CURRENT_USER\SOFTWARE\Policies\Microsoft\Windows`  

Add key `Explorer`  

Add Dword32 `DisableSearchBoxSuggestions`  

Set Value to 1




=======
Double click it and set the value to 1
>>>>>>> dd574b9baef2e9804fbf60218ef1cba61218c4c9


