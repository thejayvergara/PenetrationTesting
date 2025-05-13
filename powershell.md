# POWERSHELL
## Help
```powershell
get-help get-wmiobject
```
## Windows Management Instrumentation (WMI)
```powershell
get-wmiobject win32_operatingsystem
get-wmiobject win32_useraccount
get-wmiobject win32_startupcommand
get-wmiobject win32_service
```

## Registry
```powershell
get-itemproperty "HKCU:\Software\Microsoft\Windows\CurrentVersion\Run"
```

## Groups
```powershell
get-localgroup
```
