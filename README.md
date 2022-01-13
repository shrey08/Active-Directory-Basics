# Active-Directory-Basics
## Introduction
1.	Directory service for Windows Domain Networks.
2.	Collection of machines and servers connected inside of domains.

### Use of Active Directory:
- Control and monitoring of their user's computers through a single domain controller.
- Allows for any user in the company to use any machine that the company owns, without having to set up multiple users on a machine.

## Physical Active Directory:
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
+ Contains <blockquote>NTDS.dit</blockquote>
  + a database that contains all of the information of an Active Directory domain controller as well as password hashes for domain users
- Stored by default in <blockquote>%SystemRoot%\NTDS</blockquote>
- Accessible only by the domain controller

## Forest
A forest is a collection of one or more domain trees inside of an Active Directory network. It is what categorizes the parts of the network as a whole.

### Consists of:
#### Trees
> A hierarchy of domains in Active Directory Domain Services
#### Domains
> Used to group and manage objects 
#### Organizational Units (OUs)
> Containers for groups, computers, users, printers and other OUs
#### Trusts
> Allows users to access resources in other domains
#### Objects
> Users, groups, printers, computers, shares
#### Domain Services
> DNS Server, LLMNR, IPv6
#### Domain Schema
> Rules for object creation

## Users + Groups
When you create a domain controller it comes with default groups and two default users: Administrator and guest.

### Types of users:
- Domain Admins
- Service Accounts (Can be Domain Admins)
- Local Administrators
- Domain Users

### Types of groups:
- Security Groups
- Distribution Groups

### Default Security Groups:
- Domain Controllers
- Domain Guests
- Domain Users
- Domain Computers
- Domain Admins
- Enterprise Admins
- Schema Admins
- DNS Admins
- DNS Update Proxy
- Allowed RODC Password Replication Group
- Group Policy Creator Owners
- Denied RODC Password Replication Group
- Protected Users
- Cert Publishers
- Read-Only Domain Controllers
- Enterprise Read-Only Domain Controllers
- Key Admins
- Enterprise Key Admins
- Cloneable Domain Controllers
- RAS and IAS Servers

## Trust + Policies

>Trusts
Mechanism in place for users in the network to gain access to other resources in the domain.
Two types of trusts that determine how the domains communicate:
- <b>Directional</b> - The direction of the trust flows from a trusting domain to a trusted domain
- <b>Transitive</b> - The trust relationship expands beyond just two domains to include other trusted domains

>Policies
Simply act as a rulebook for Active  Directory that a domain admin can modify and alter as they deem necessary to keep the network running smoothly and securely.
A few policies:
- <b>Disable Windows Defender</b> - Disables windows defender across all machine on the domain
- <b>Digitally Sign Communication (Always)</b> - Can disable or enable SMB signing on the domain controller

## Active Directory Domain Services + Authentication
Default Domain Services:
- LDAP - Lightweight Directory Access Protocol; provides communication between applications and directory services
- Certificate Services - allows the domain controller to create, validate, and revoke public key certificates
- DNS, LLMNR, NBT-NS - Domain Name Services for identifying IP hostnames

Two main types of authentication in place for Active Directory:
- Kerberos - The default authentication service for Active Directory uses ticket-granting tickets and service tickets to authenticate users and give users access to other resources across the domain.
- NTLM - default Windows authentication protocol uses an encrypted challenge/response protocol

## AD in Cloud
| Windows Server AD  | Azure AD |
| ------------- | ------------- |
| LDAP  | Rest APIs  |
| NTLM  | NTLM	OAuth/SAML  |
| Kerberos  | OpenID  |
| OU Tree  | Flat Structure  |
| Domains and Forests  | Tenants  |
| Trusts  | Guests  |
