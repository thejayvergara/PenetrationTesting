# WINDOWS ENUMERATION
### QUESTIONS TO ANSWER:
1. What system information can we pull from our target host?
2. What other system(s) is our target host interacting with over the network?
3. What user account(s) do we have access to, and what information is accessible from the account(s)?

### THINGS TO LOOK FOR:
1. **General System Information**
   - Hostname
   - OS Information
     - Name
     - Version
     - Configuration
     - Installed Patches/Hotfixes
2. **Networking Information**
   - Network Interfaces
   - IP addresses
   - Accessible Subnets
   - DNS Servers (/etc/resolv.conf)
   - Known Hosts (/etc/hosts)
   - Network Resources
     - Network Shares
     - Domain Resources
     - Network Devices
   - Firewall Configuration
3. **Basic Domain Information**
   - Domain/Workgroup Name
   - Logon Server
4. **User Information**
   - User Accounts
   - Local Groups
   - Environment Variables
   - Available Tasks
     - Running Tasks
     - Scheduled Tasks
   - Available Services
     - Anti-Virus Solitions
     - IDS/IPS


## GENERAL SYSTEM INFORMATION:
```cmd
systeminfo
```

### Hostname
```cmd
hostname
```

### Version
```cmd
ver
```



## NETWORKING INFORMATION:
### Networking interfaces and IP Adrresses
```cmd
ipconfig /all
```

### ARP Cache
```cmd
arp /a
```

### Network shares on the host
```cmd
net share
```

### Network shares the host knows of
```cmd
net view
```



## USER INFORMATION
### Current user information
```cmd
whoami /all
```

### Network share users
```cmd
net user
```

### Network share groups
```cmd
net group
```



## SEARCHING FOR FILES
```cmd
where /r %directory% %file_to_find%
```

## SEARCHING FOR STRINGS WITHIN A FILE (SIMILAR TO `grep`)
```cmd
findstr %string_to_search% %file%
```
