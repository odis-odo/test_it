# Get-CimInstance

[Video](https://www.youtube.com/watch?v=HbT7GhkOQI8)
[Video2](https://www.youtube.com/watch?v=K-naZ8ZjhpU)


## Basic Syntax

```Powershell
#Get operating system information
Get-CimInstance -Classname Win32_OperatingSystem
```

&nbsp;

## Common Examples

```Powershell
#Get Computer System Details
Get-CimInstance -ClassName Win32_ComputerSystem
```

```Powershell
#Get Processor Information 
Get-CimInstance -ClassName Win32_Processor
```

&nbsp;

## Filtering Results

```Powershell
#Using -Filter Parameter
Get-CimInstance -ClassName Win32_Service -Filter "State = 'Running'"
```

```Powershell
#Using Where-Object
Get-CimInstance -ClassName Win32_Process | Where-Object {$_.Name -like "*chrome*"}
```

&nbsp;  

## Remote Queries  

```Powershell
#Query Single Remote Computer
Get-CimInstance -ClassName Win32_BIOS -ComputerName "Server01"
```

```Powershell
#Query Multiple Remote Computers
Get-CimInstance -ClassName Win32_LogicalDisk -ComputerName "Server01", "Server02"
