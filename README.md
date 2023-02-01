
<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop
- Active Directory Domain Services
- PowerShell ISE

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Create Azure Virtual Machine and Run it with Remote Desktop
- Install Active Directory Domain Services on Domain Controller
- Create Randomly Generated Users

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/TexrKCW.png" height="60%" width="60%" alt="Virtual Machines"/>
</p>
<p>
To begin, we must first start by creating and running a Virtual Machine in Microsoft Azure. 2 actually, one for the Domain Controller and another for a user we will create later. Both VM's are created with Windows 10 and using 2 vcpu's on each since we're limited to 4 vcpu's on a free Microsoft Azure account. Once the VM's are created and running, we start up Remote Desktop, we use the username and password that we created for the VM to login. It's here in DC where we install Active Directory.
</p>
<br />

<p>
<img src="https://i.imgur.com/fDJRcba.png" height="60%" width="60%" alt="Install Active Directory"/>
</p>
<p>
Now that the Domain Controller is set and running in Remote Desktop, we install Active Directory Domain Services and Powershell ISE. During this step, we have to enable a few things in order to have it running correctly, otherwise we won't be able to create users or even run Active Directory. After all is set and done, we run a special code in Powershell ISE to generate about a thousand "users" that share the same password.
</p>
<br />

<p>
<img src="https://imgur.com/5ru15Cp.png" height="80%" width="80%" alt="Creating Users"/>
</p>
<p>
Now that the users are being created from the previous step, we can utilize the second Virtual Machine to login into any one of many users that were just created. Hopping back into DC, we can manipulate the security levels of the user on the other machine. We can dabble in some file sharing and permissions during this step. As the Domain Controller, we can assign security levels and permissions such as viewing documents and if they're able to edit or just view. Or even view different documents and folders in the same network/server.
</p>
<br />
