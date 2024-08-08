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
- Create additional users and attempt to log into client-1 with one of the users

<h2>Deployment and Configuration Steps</h2>

<p>
<b>1.) Setup Resources in Azure</b>
  
- Create the Domain Controller VM (Windows Server 2022) named “DC-1”
- Take note of the Resource Group and Virtual Network (Vnet) that get created at this time
- Set Domain Controller’s NIC Private IP address to be static
- Create the Client VM (Windows 10) named “Client-1”. Use the same Resource Group and Vnet that was created
- Ensure that both VMs are in the same Vnet
</p>

<p>
<b>2.) Ensure Connectivity between the client and Domain Controller</b>
  
- Login to Client-1 with Remote Desktop and ping DC-1’s private IP address with ping 10.0.0.4.
- Login to the Domain Controller and enable ICMPv4 in on the local windows Firewall
- Check back at Client-1 to see the ping succeed

</p>











<p>
<img src="https://i.imgur.com/j0afGUZ.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/mHfYtf0.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
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
<img src="https://i.imgur.com/xIP3UTI.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/kzsJOvW.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/o1OzFWp.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
https://i.imgur.com/i6lfMVE.png
https://i.imgur.com/d2ZI7xZ.png
https://i.imgur.com/iyGGU7V.png
https://i.imgur.com/3UbJGYi.png
https://i.imgur.com/HG1NzTp.png

<p>
<img src="https://i.imgur.com/Tnf46S2.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
https://i.imgur.com/RrQmqBp.png
https://i.imgur.com/xzRW3F6.png
https://i.imgur.com/bIAmIx2.png
https://i.imgur.com/VM6ytZn.png
https://i.imgur.com/zl5HLii.png



