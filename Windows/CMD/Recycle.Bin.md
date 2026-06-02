

To view contents of recycle bin in cmd use the following command:  

```
dir C:\$Recycle.Bin /s /b
```

- The `/s` option  displays files in specified directory and all subdirectories
- The `/b` option  uses bare format (no heading information or summary)   

<br>

## Powershell  


 The direct PowerShell equivalent to `dir C:\$Recycle.Bin /s /b` is:  

```powershell 
Get-ChildItem -Path 'C:\$Recycle.Bin' -Force -Recurse | ForEach-Object { $_.FullName }   
```  

### Key Differences & Notes:  

- **`-Force` is required**: The `$Recycle.Bin` folder is a **hidden** and **system** attribute folder.  Without `-Force`, `Get-ChildItem` will not see or enter it.  
  <br>
- **`ForEach-Object { $_.FullName }`**: The `/b` (bare format) switch in CMD outputs only the full path. In PowerShell, `Get-ChildItem` returns objects. Piping to `ForEach-Object { $_.FullName }` extracts just the string path, mimicking the CMD output.   
   <br>
- **Alternative for just the directory itself**: If you only need to list the `$Recycle.Bin` folder (not its contents) in bare format, use:  

```powershell
Get-Item -Path 'C:\$Recycle.Bin' -Force | ForEach-Object { $_.FullName }   

```