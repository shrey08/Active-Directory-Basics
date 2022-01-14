## Hands-On Lab (TryHackMe)
Active Directory by using PowerShell commands to view machines, computers, users, and groups.

### Lab Setup:
1. Deploy the machine
2. SSH or RDP into the machine (or use the browser-based instance)
> Username:  
Password:  
Domain: CONTROLLER.local

### PowerView Setup:
1. ```Powershell cd Downloads``` - navigate to the directory PowerView is in
2. ```Powershell powershell -ep bypass``` - load a powershell shell with execution policy bypassed
3. ```Powershell . .\PowerView.ps1``` - import the PowerView module
