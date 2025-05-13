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
(cp) copy-item
(clear) clear-host
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

# Key and Value
get-itemproperty registry::hkcu\software\microsoft\windows\currentversion\runonce

# Add key
new-item hkcu:\software\microsoft\windows\currentversion\runonce -name $key

# Add value
new-itemproperty hkcu:\software\microsoft\windows\currentversion\runonce\$key -name $value

# Remove key
remove-item hkcu:\software\microsoft\windows\currentversion\runonce -name $key

#Remove value
remove-itemproperty hkcu:\software\microsoft\windows\currentversion\runonce\$key -name $value
```


## Module Extensions
.ps1 -- Powershell Main File \
.psd1 -- Powershell Data File \
.psm1 -- Powershell Script File
