### About
- Servers and machines on-premise.
- Can be anything from doamin controllers & storage servers to user's domain machine; everything needed for an Active Directory environment besides the software.

### Domain Controller
Windows server that has Active Directory Domain Services (AD DS) installed and has been promoted to a domain controller in the forest.
- Holds the AD DS data store
- Handles authentication and authorization services 
- Replicate updates from other domain controllers in the forest
- Allows admin access to manage domain resources

### AD DS Data Store
Holds the databases and processes needed to store and manage directory information such as users, groups, and services.
- Contains <blockquote>NTDS.dit</blockquote>
- - a database that contains all of the information of an Active Directory domain controller as well as password hashes for domain users
- Stored by default in > %SystemRoot%\NTDS
- Accessible only by the domain controller
