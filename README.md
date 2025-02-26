<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1> Active Directory - Deployment/Post-Installation Configuration</h1>
This tutorial outlines the deployment of on-premises Active Directory within two Azure virtual machines. <br/>
<br/>
<p align="center">
<img height ="80% ="<img width="40%" alt="Screenshot 2025-02-25 at 4 05 26 PM" src="https://github.com/user-attachments/assets/effe8a9b-6c87-4011-9da1-e041a08a700b" /> <br/>


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

Create a Domain Admin user within the domain > Navigate to start and go into Active Directory Users and Computers: 
<p align="center"> 
<img alt="Screenshot 2025-02-26 at 12 33 47 AM" src="https://github.com/user-attachments/assets/19f1dc58-0b24-463a-a7b4-070883d5af71"  height="80%" width="80%" />


    
In Active Directory Users and Computers (ADUC), create an Organizational Unit (OU) called “_EMPLOYEES”:
<p align="center"> 
<img alt ="Screenshot 2025-02-26 at 12 34 12 AM" src="https://github.com/user-attachments/assets/8cd0ff40-007f-4620-8bfc-1eca2a718dc2" height="80%" width="80%" />
" />
<br />
<p align="center"> 

Create a new OU named “_ADMINS":
<p align="center"> 
<img alt="Screenshot 2025-02-26 at 12 35 20 AM" src="https://github.com/user-attachments/assets/2eaf444b-5baa-4807-ab1d-28e2937aaf62" height="80%" width="80%"/>



Create a new employee named “Jane Doe” (same password) with the username of “jane_admin” / Cyberlab123!
<p align="center"> 
<img alt="Screenshot 2025-02-26 at 12 35 40 AM" src="https://github.com/user-attachments/assets/495790e9-f297-4f58-a3cc-4f00fdbb2402" height="80%" width="80%"/>



<p align="center"> 
<img alt="Screenshot 2025-02-26 at 12 36 44 AM" src="https://github.com/user-attachments/assets/45ba76dc-8177-4af6-a21f-870756add993" height="80%" width="80%"/>



Add jane_admin to the “Domain Admins” Security Group
<p align="center">
<img alt="Screenshot 2025-02-26 at 12 37 22 AM" src="https://github.com/user-attachments/assets/9ecf10e1-6252-4eaa-a2ce-0e94c4e52233" height="80%" width="80%">


<img alt="Screenshot 2025-02-26 at 12 39 33 AM" src="https://github.com/user-attachments/assets/b971ef2c-7aa5-40ea-96ff-057c698253cd" height="80%" width="80%"/>


<p align="center">

Log out / close the connection to DC-1 and log back in as “mydomain.com\jane_admin”. User jane_admin as your admin account from now on:
<p align="center"> 
<img =alt="Screenshot 2025-02-26 at 12 40 14 AM" src="https://github.com/user-attachments/assets/b85fb626-3532-4de4-a2e5-318632835651" height="80%" width="80%"/>

Join Client-1 to your domain (mydomain.com) > Login to Client-1 as the original local admin (labuser) and join it to the domain:
<p align="center"> 
start > system  

<p align="center"> 
<img alt="Screenshot 2025-02-26 at 12 41 33 AM" src="https://github.com/user-attachments/assets/6d48482e-3df7-4b54-b6d2-9a160f23bc7d" height="80%" width="80%" />
<img alt="Screenshot 2025-02-26 at 12 41 13 AM" src="https://github.com/user-attachments/assets/f807c3a6-bf67-4277-82f4-595a0cadc60e" height="80%" width="80%" />



Login to the Domain Controller and verify Client-1 shows up in Active Directory Users and Computers: 
<p align="center"> 
<img alt="Screenshot 2025-02-26 at 12 41 55 AM" src="https://github.com/user-attachments/assets/e157362a-b976-4e80-9261-c746d8ba0c30" height="80%" width="80%"  />

  
Create a new OU named “_CLIENTS” and drag Client-1 into there  > Right click mydomain > New > Organizational unit > Type _CLIENTS:
<p align="center"> 
<img alt="Screenshot 2025-02-26 at 12 42 14 AM" src="https://github.com/user-attachments/assets/c02c11ba-7066-4dbd-b7ea-eb634acd08f4" height="80%" width="80%"  />

<b> Congratulations we have finished the completion of the deployment, we will continue with group poilcies in part 3!

