<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1> Active Directory - Deployment/Post-Installation Configuration</h1>
This tutorial outlines the deployment of on-premises Active Directory within two Azure virtual machines. <br/>

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>Program walk-through</h2>
<br />

<p align="center">
Create a Domain Admin user within the domain > Navigate to start and go into Active Directory Users and Computers: 
<p align="center"> 
<img src="https://i.imgur.com/kxTxhCf.png" height="80%" width="80%" 
<br />
<br />   
In Active Directory Users and Computers (ADUC), create an Organizational Unit (OU) called “_EMPLOYEES”:
<img src="https://i.imgur.com/Cwazh9r.png" height="80%" width="80%" 
<br />
<br />
Create a new OU named “_ADMINS": 
<img src="https://i.imgur.com/l9LYU9t.png" height="80%" width="80%" 
<br />
<br />
Create a new employee named “Jane Doe” (same password) with the username of “jane_admin” / Cyberlab123!
<img src="https://i.imgur.com/wUg470J.png" height="80%" width="80%" 
<br />
<br />
<img src="https://i.imgur.com/ZEnw7QB.png" height="80%" width="80%" 
<br />
<br />
Add jane_admin to the “Domain Admins” Security Group    
<img src="https://i.imgur.com/ekYGH43.png" height="80%" width="80%" 
<br />
<br />
<img src="https://i.imgur.com/1tOuDmq.png" height="80%" width="80%" 
<br />
<br />
Log out / close the connection to DC-1 and log back in as “mydomain.com\jane_admin”. User jane_admin as your admin account from now on:
<img src="https://i.imgur.com/4rtJzfF.png" height="80%" width="80%" 
<br />
<br />
Join Client-1 to your domain (mydomain.com) > Login to Client-1 as the original local admin (labuser) and join domain:
<p align="center">
<img src="https://i.imgur.com/cZB0QKv.png" height="80%" width="80%" 
<br />
<br />
<img src="https://i.imgur.com/tPGvuMq.png" height="80%" width="80%" 
<br />
<br />
Login to the Domain Controller and verify Client-1 shows up in Active Directory Users and Computers: 
<img src="https://i.imgur.com/ebM02yY.png" height="80%" width="80%" 
<br />
<br />
Create a new OU named “_CLIENTS” and drag Client-1 into there  > Right click mydomain > New > Organizational unit > Type _CLIENTS:
<p align="center">
<img src="https://i.imgur.com/EfUBeqH.png" height="80%" width="80%" 
<br />
<br />


<b> Congratulations we have finished the completion of the deployment, we will continue with group poilcies in 
[part 3!](https://github.com/AnthonydcHo/usersactivedirectory) 

