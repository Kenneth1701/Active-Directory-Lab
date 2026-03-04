# Active-Directory-Lab
This is Home lab that I design to extend my knowledge in Active Directory and DNS 
To begin this lab I Installed Windows Server 2022 ISO and Windows 10 Enterprise ISO. I downloaded the VMWare for the hypervisor to virtualise Windows Server 2022 and Windows 10 Enterprise

Installing Windows Server 2022 ISO
<img width="1919" height="956" alt="Image" src="https://github.com/user-attachments/assets/230a7390-8318-426b-a796-ba459c7d99c2" />

Accsess to the Server Manager
<img width="1919" height="957" alt="Image" src="https://github.com/user-attachments/assets/7640ad86-a7cb-42f0-8491-2e6726ed9e1d" />

Configuring the Network Settings
  I configured my Windows server with:
    - Customise computer name
    - Domain name: trinity.com
    - Remote Desktop Enabled
    - Static Ip address: 192.168.58.3 /24
    - Subnet Mask: 255.255.255.0
    - IP default gateway: 192.168.58.2 /24
    - DNS IP address: 127.0.0.1 (this address means that the dns server is pointing to its ownself)
<img width="1718" height="865" alt="Image" src="https://github.com/user-attachments/assets/55417860-56de-4b55-a5b1-6188a19bd98f" />

Logging in using Domain Admin account
AFter configuring all of the things above I restarted the Windows Server. After restarting the Server requires to log in using domain admin which in my case is TRINITY\Admin
