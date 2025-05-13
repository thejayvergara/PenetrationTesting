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
