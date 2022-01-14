## Hands-On Lab (TryHackMe)
Active Directory by using PowerShell commands to view machines, computers, users, and groups.

### Lab Setup:
1. Deploy the machine
2. SSH or RDP into the machine (or use the browser-based instance)
> Username:  
Password:  
Domain: CONTROLLER.local

### PowerView Setup:
1. ```ps
cd Downloads
``` 
- navigate to the directory PowerView is in
5. ```ps powershell -ep bypass ``` - load a powershell shell with execution policy bypassed
6. ```ps . .\PowerView.ps1 ``` - import the PowerView module <br/>
![image](https://user-images.githubusercontent.com/35620941/149575780-70ca473b-442a-47f1-858c-4cbd82e6ee4e.png)

### Lab:
- ```Powershell Get-NetComputer -fulldata | select operatingsystem``` - gets a list of all operating systems on the domain
![image](https://user-images.githubusercontent.com/35620941/149576088-bb27894e-6ec1-4ea1-896a-8f348b24c345.png)

- ```Powershell Get-NetUser | select cn``` - gets a list of all users on the domain
![image](https://user-images.githubusercontent.com/35620941/149576135-9ad0eb5c-1268-46d3-b6a2-fcd4b4874583.png)
