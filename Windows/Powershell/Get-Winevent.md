# Get-Winevent

[Tutorial](https://www.youtube.com/watch?v=TZOtIs0zsKM)

## Basic Syntax

```Powershell
#Get the most recent 10 events from Application log
Get-WinEvent -LogName 'Application' -Maxevents 10
```

```Powershell
#List all available event logs
Get-WinEvent -Listlog *
```

&nbsp;

## Common Log Names

- `Application` -Application events and errors
    
- `Security` - Audit and security events
    
- `System` - System component events
    
- `Setup` - Installation and setup logs
    
<br>

## Filtering with FilterHashtable

```Powershell
# Get Errors from last 24 hours
Get-WinEvent -FilterHashtable @{
  Logname = 'Application'
  Level = 2
  StartTime = (Get-date).AddDays(-1)
}
```

&nbsp;

## Event Levels

- `Critical` = 1
    
- `Error` = 2
    
- `Warning` = 3
    
- `Information` = 4
    

## Advanced Filtering

```Powershell
# Filter by provider and event ID
Get-WinEvent -FilterHashtable @{
   Logname = 'System'
   ProviderName = 'Microsoft-Windows-Kernel-Power'
   ID = 41
   StartTime = (Get-Date).AddDays(-7)
}
```