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

## Module Extensions
.ps1 -- Powershell Main File \
.psd1 -- Powershell Data File \
.psm1 -- Powershell Script File
