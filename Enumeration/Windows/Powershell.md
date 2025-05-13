# POWERSHELL ENUMERATION
### Powershell command history
```powershell
get-content c:\users\%username%\AppData\Roaming\Microsoft\Windows\PowerShell\PSReadLine\ConsoleHost_history.txt
```

### Powershell modules
```powershell
# Installed and LOADED in our current session
get-module

# Installed but NOT LOADED in our current session
get-module -listavailable
```

### Powershell Module Path
```powershell
$env:PSModulePath
```

### Powershell Execution Policy
```powershell
get-executionpolicy -list
```

## USER ACCOUNTS
Local Users
```powershell
get-localuser
```

Local Groups
```powershell
# Local Groups
get-localgroup

# Users under a local group
get-localgroup -name $localgroup_name
```
