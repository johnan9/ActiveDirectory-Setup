<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Setup Resources in Azure
- Ensure Connectivity between the client and Domain Controller
- Install Active Directory
- Create an Admin and Normal User Account in AD
- Join Client-1 to your domain (mydomain.com)
- Setup Remote Desktop for non-administrative users on Client-1
- Create additional users and attempt to log into Client-1 with one of the users

<h2>Deployment and Configuration Steps</h2>

<p>
<b>1.) Setup Resources in Azure</b>
  
- Give the Resource Group name <b>RG-Lab-AD</b>
- Create the Domain Controller VM (Windows Server 2022) named <b>DC-1</b>
- Set Domain Controller’s NIC Private IP address to be <b>static</b>
- Create the Client VM (Windows 10) named <b>Client-1</b>. Use the same Resource Group and Vnet that was created.
</p>
<p>
<img src="https://i.imgur.com/j0afGUZ.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/k9jw8o0.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/ars1TsV.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/VSSvcYV.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>

<p>
<b>2.) Ensure Connectivity between the client and Domain Controller</b>
  
- Login to the Domain Controller and enable ICMPv4 in on the local windows Firewall
- Login to Client-1 with Remote Desktop and ping DC-1’s private IP address with ping 10.0.0.4.
- Check that the Client-1 to see the ping succeed
</p>
<p>
<img src="https://i.imgur.com/xIP3UTI.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/kzsJOvW.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/o1OzFWp.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>

<p>
<b>3.) Install Active Directory</b>
  
- In DC-1, on the Server Manager, navigate to <b>Manage</b> > <b>Add Roles and Features</b>
- Install <b>Active Directory Domain Services</b>
- <b>Promote as a DC</b> and setup a new forest as <b>mydomain.com</b>
- Restart and then log back into DC-1 as user: <b>mydomain.com\johnan</b>
</p>
<p>
<img src="https://i.imgur.com/mHfYtf0.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/i6lfMVE.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/d2ZI7xZ.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/iyGGU7V.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/3UbJGYi.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/HG1NzTp.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>



<p>
<b>4.)Create an Admin and Normal User Account in AD</b>

- In Active Directory Users and Computers (ADUC), create an Organizational Unit (OU) called <b>_EMPLOYEES</b>
- Create a new OU named <b>_ADMINS</b>
- Create a new employee named <b>Jane Doe</b> with the username of <b>jane_admin</b>, password <b>Password1</b>
- Add <b>jane_admin</b> to the "Domain Admins” Security Group
- Log out/close the Remote Desktop connection to DC-1 and log back in as <b>mydomain.com\jane_admin</b>
- User </b>jane_admin<b> as your admin account from now on
</p>





<p>
<img src="https://i.imgur.com/Tnf46S2.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/xzRW3F6.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/RrQmqBp.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/bIAmIx2.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/VM6ytZn.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>




<p>
<img src="https://i.imgur.com/zl5HLii.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
https://i.imgur.com/GepRcQB.png
https://i.imgur.com/9VyDQCo.png
https://i.imgur.com/6diV6ew.png
https://i.imgur.com/t6RlyMI.png
https://i.imgur.com/lOsAGPg.png
https://i.imgur.com/chslPWR.png
https://i.imgur.com/3ASl7ew.png
https://i.imgur.com/LapN0bd.png
https://i.imgur.com/fksT6hl.png
https://i.imgur.com/5jthMZq.png
https://i.imgur.com/SUyYMad.png
https://i.imgur.com/1lK9AWh.png
https://i.imgur.com/K4Hq8Lr.png
https://i.imgur.com/4BAJlJT.png
https://i.imgur.com/ZiW8cQV.png

