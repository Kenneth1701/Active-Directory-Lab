# Active-Directory-Lab
Overview
This project demonstrates the design and implemntation of a Windows Active Dierectory Lab environment simulating a real-world enterprise network 
The lab focuses not only on core Active Directory services but also on real troubleshooting scenarios, including authentication issues, DNS behavio, password reset and file share permission conflicts. 

Objectives
- Deploy and configure Active Directory Domain Services
- Configure DNS for proper hostname resolution
- Join client machines to the domain
- Create and manage users and security groups
- Configure shared folders with controlled access
- Troubleshoot access and authentication issues

Lab Architecture
Environment Setup:
- Domain Controler (Windows Server)
- Client Machine

Key Components: 
- Active Directory Domain Services
- DNS Server
- File Sharing System

Access Flow: 
Client -> Domain Controller -> Authentication -> Shared Folder Access

Technologies Used
- Windows Server 2022
- Active Directory Domain Services
- DNS
- File Sharing
- Virtual Machine (VMWare

Key Configuration
Domain Controllet Setup
- Installed Active Directory Domain Services
- Promoted server to Domain Controller
- Configured domain environment
https://github.com/Kenneth1701/Active-Directory-Lab/blob/85c74cb61ae1deeb6e4b956fe69b70c7b1de928a/Setting%20up%20Static%20Ip%20address%20and%20DS.png

Client Domain Join
- Connected client machine to the domain
- Verified domain authentication
- Tested connectivity using:
    - ping
    - SMB access
User & Group Management
- Created domain users
- Added users into security group
- Used group-based access control for resource management

File Sharing & Permission 
- Created shared folder on Domain Controller
- Configured:
    - Share permissions
    - NTFS permissions
- Assigned access via security groups

Troubleshoting Scenarios
Scenario 1: User Cannot Access Shared Folder
Issue
- User could see the shared folder
- Unable to read or write inside the folder
- Permissions appeared correctly configured

 Investigation 
 - Verivied:
   - User is part of the correct security group
   - Share permissions are correctly assigned
   - NTFS permssions allow access
  -  Confirmed no obvious misconfiguration in access control
  -  Issues persisted despite correct configuration

Root Cause
- The client machine had not refreshed its authentication token / group membership
- Changes to user group membership were not applied immediately
- System required a session refresh to update permission

Resolution 
- Restarted the client machine
- User logged back into the domain
- Group membership and permission refreshed
- Access to shared folder (read/write) successfully restored



