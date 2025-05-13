# POWERSHELL CHEATSHEET
## HELP COMMANDS
```powershell
get-help
get-command -verb get
get-command -noun windows*
get-command -module powershellget
```

## (LINUX EQUIVALENT) POWERSHELL
```powershell
(alias) get-alias
(cat) get-content
(cd) set-location
(clear) clear-host
(cp) copy-item
(curl) invoke-webrequest
(grep) select-string
(history) get-history
(ls) get-childitem
(mkdir) new-item
(pwd) get-location 
(rm) remove-item
```

## FILTERING, SORTING, AND GROUPING
```powershell
$command | get-member
$command | select-object $property1,$property2
$command | sort-object $property1 | group-object $property2
$command | where $property_value -like '*$search_string*'
```

## INSTALLING MODULES
```powershell
# Available commands to use Powershell Gallery
get-command -module powershellget

# Looking for a module
find-module -name admintoolbox

# Installing module
install-module admintoolbox
```

## REMOTE COMMAND
```powershell
invoke-command -computername $hostname -scriptblock {$command}
```

## REGISTRY
```powershell
# Display Directories
get-childitem registry::hkcu\software\microsoft\windows\currentversion

# Display Key and Value
get-itemproperty registry::hkcu\software\microsoft\windows\currentversion\runonce

# Add key
new-item hkcu:\software\microsoft\windows\currentversion\runonce -name $key

# Add value
new-itemproperty hkcu:\software\microsoft\windows\currentversion\runonce\$key -name $value

# Remove key
remove-item hkcu:\software\microsoft\windows\currentversion\runonce -name $key

# Remove value
remove-itemproperty hkcu:\software\microsoft\windows\currentversion\runonce\$key -name $value
```


## Event Logs
```powershell
get-winevent -ListLog Security
```

## HTTP Requests
```powershell
invoke-webrequest $url -method get
```


## Module Extensions
.ps1 -- Executable Powershell scripts
.psd1 -- Powershell Data file
.psm1 -- Powershell Module File
