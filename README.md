<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)
<h2>Overall steps</h2>
<h3></h3> 1) Create virtual machine in azure
<h4></h4> 2) Install and enable IIS
<h5></h5> 3) Install the prereqs
<h6></h6> 4) Open IIS
<h7></h7> 5) Continue installing prereqs
<h8></h8> 6) Setup osTicket in the browser
<h9></h9> 7) Check user and local host osTicket URLs

 
<h2>Installation Steps</h2>

![image](https://github.com/boluadunbarin/osticket-prereqs3/assets/157642328/82678fc5-de9f-47d0-93b7-28318a7be4a7)

Create a virtual machine in azure, windows 10, 4vCPUs
Name: vm-osticket

User: gftbnd

Password:abdABD1!EJFejf

![Screenshot 2024-01-24 220958](https://github.com/boluadunbarin/osticket-prereqs3/assets/157642328/c5967489-eb10-4f6f-8a6c-1e1c1910c32c)

Files to download

![Screenshot 2024-01-24 221218](https://github.com/boluadunbarin/osticket-prereqs3/assets/157642328/bef9bb83-98a6-4822-b841-32e98835ecf0)

IIS> world wide web services> application development features> (x) CGI
IIS> world wide web services> (x) common http features

Install (PHPManagerForIIS_V1.5.0.msi)

Install (rewrite_amd64_en-US.msi)

![1](https://github.com/boluadunbarin/osticket-prereqs3/assets/157642328/2f607629-ac8c-476c-b950-9f661d7d7012)

Create PHP folder in C-drive

![2](https://github.com/boluadunbarin/osticket-prereqs3/assets/157642328/7d526d2e-a4a0-4e27-887a-8fe20a1a4ccb)

Download (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into the c:\php folder

Download and install (VC_redist.x86.exe.)

![3](https://github.com/boluadunbarin/osticket-prereqs3/assets/157642328/b1538b08-b75a-4016-a42e-1f09504d1b17)

Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi)

![4](https://github.com/boluadunbarin/osticket-prereqs3/assets/157642328/110b0ec2-f06e-4e05-aaf1-81b4dea71dc8)

![5](https://github.com/boluadunbarin/osticket-prereqs3/assets/157642328/0b2d0caf-b5e2-4883-88a6-d7ec0da507e4)
Open IIS as admin

![6](https://github.com/boluadunbarin/osticket-prereqs3/assets/157642328/6ad8a45d-80bd-4000-94a0-6e5baac4655c)

![7](https://github.com/boluadunbarin/osticket-prereqs3/assets/157642328/284a35d4-737b-487c-b4d3-80a30e2093fe)

Register PHP from within IIS

![8](https://github.com/boluadunbarin/osticket-prereqs3/assets/157642328/7b797ece-4d1a-451c-bb70-a1ad5f236c0c)

Reload IIS (restart the server)

![9](https://github.com/boluadunbarin/osticket-prereqs3/assets/157642328/5c5a3ce0-c60f-44b9-ba32-d8b759cc023d)


![10](https://github.com/boluadunbarin/osticket-prereqs3/assets/157642328/f1a2e0d6-ee30-46e9-9dda-7edf3f820fd3)

Download osTicket
Copy “upload” folder to c:\inetpub\wwwroot
Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”

Reload IIS (restart the server)

![11](https://github.com/boluadunbarin/osticket-prereqs3/assets/157642328/bb2ab875-8228-49f1-86d9-fc7ce0dc3c43)

Go to sites -> Default -> osTicket
On the right, click “Browse *:80”

![12](https://github.com/boluadunbarin/osticket-prereqs3/assets/157642328/6fffcf7c-2f18-44e8-aea6-b5ebe437289b)

![13](https://github.com/boluadunbarin/osticket-prereqs3/assets/157642328/3a0218a3-6e68-42e9-9925-a867677a5a5f)

![14](https://github.com/boluadunbarin/osticket-prereqs3/assets/157642328/a88df853-0d92-4a14-bfcc-d9f43747d62b)
Check the osticket website from the “Browse *:80” step

![15](https://github.com/boluadunbarin/osticket-prereqs3/assets/157642328/86ad4eca-9145-4757-97c6-087d25ad0f82)

Rename: ost-config.php

From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php

To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

Assign Permissions: ost-config.php

Disable inheritance:  Remove All

New Permissions: Everyone: All

![18](https://github.com/boluadunbarin/osticket-prereqs3/assets/157642328/4ad75467-3b4a-4f54-8a7f-796b1771078d)

Create a database called osticket

![17](https://github.com/boluadunbarin/osticket-prereqs3/assets/157642328/8233fc0f-f1d8-48c9-b5a4-deff3dc377c2)

Continue Setting up osticket in the browser

MySQL Database: osTicket

MySQL Username: root

MySQL Password: Password1

Click “Install Now!”

Browse to http://localhost/osTicket/scp/login.php  for agent/admin 

Browse to http://localhost/osTicket/ for  End Users osTicket URL 
