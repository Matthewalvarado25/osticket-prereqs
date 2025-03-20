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

<h2>List of Prerequisites</h2>

-  Set Up an Azure Virtual Machine
-  Download osticket instalation files within the virtual machine
-  Enable IIS in Windows with CGI
-  Install PHP manager for IIS from the osTicket Installation Files
-  Install the Rewrite Module from the osTicket Installation Files
-  Install VC_redistx86 from the osTicket Installation Files
-  Install MYSQL 5.5.62 from the osTicket Installation Files
-  Install HeidiSQL from the osTicket Installation Files
<h2>Installation Steps</h2>
<h3>Step:1 Create a Virtual Machine(VM) in Azure</h3>

<p>
  
- Create a resource group in Azure
- Create a virtual machine
    - Under Image, select Windows 10 Pro version 22H2
    - Under Size, select option with at least 2 vcpus
    - Create a username and password for your account
    - Review and create
</p>
<br/>

<h3>Step:2 Create a Virtual Machine(VM) in Azure</h3>

- Find your VM's public IP address and copy it
- Open the Microsoft remote desktop application
- Paste the VM's public IP address inside the computer field
  
![image](https://github.com/user-attachments/assets/50da2c37-18cd-4593-9467-0658d6d7a1ea) ![image](https://github.com/user-attachments/assets/f08829e2-05bb-4905-ba55-5f43db334036)

</p>
<br/>

<h3>Step:3 Download the osticket instalation files

- Copy the osticket files link, then inside the VM open the browser, paste a link inside the search bar, and download the files


</p>
<br/>

<h3>Step:4 Enable IIS

- Look up "control panel" on the search bar
- Open the control panel and select Programs
- Click on "Turn Windows features on or off"
- Scroll down to approve and expand "Internet Information Services(IIS)"
- Approve and expand "World Wide Web Services"
- Expand "Application Development Features"
- Approve CGI then hit "Ok"
  
  ![image](https://github.com/user-attachments/assets/8a271ebb-0905-4eb3-a677-894c4582347d)

</p>
<br/>

<h3>Step:5 Download PHP Manager 
  
- Install PHPManagerForIIS_V1.5.0.msi from the osTicket-Installation-Files folder 
  
</p>
<br/>

<h3>Step:6 Download Rewrite Module 

- Install rewrite_amd64_en-US.msi from the osTicket-Installation-Files folder 

</p>
<br/>

<h3>Step:7 Create a new Directory

- Open file explorer
- Click on "this PC"
- Navigate to the windows (C:)Drive
- In the Windows (C:) Drive, create a new folder titled "PHP"

</p>
<br/>

![image](https://github.com/user-attachments/assets/cabc0581-b7f5-495b-b93b-70a44d5881e9)


</p>
<p>
  
<h3>Step:8 Extract "php-7.3.8-nts-Win32-VC15-x86.zip"

  
</p>

- Find, "php-7.3.8-nts-Win32-VC15-x86.zip" folder in downloaded osTicket Installation Files
- Right click on the folder and choose extract all, then select the PHP folder from the (C:) Drive

![image](https://github.com/user-attachments/assets/97fa47e5-ddfa-4ba9-ab77-3a0c7bc282e0)

  
</p>
<br/>

<h3>Step:9 Install VC_redist.x86.exe
  
</p>

- Install VC_redist.x86.exe from the osticket installation files
  
<p>
  
</p>
<br/>

<h3>Step:10 Install MySQL 5.5.62
  
</p>

- Install mysql-5.5.62-win32.msi from the osticket installation files
- Choose, "typical" setup type
- Launch MYSQL Instance Configuration Wizard (after install)
- Select standard configuration
- Create and confirm a new root password 

![image](https://github.com/user-attachments/assets/8dc72ef8-cd75-4273-af42-d0aafe73bd4f)
![image](https://github.com/user-attachments/assets/acfd17d3-c78b-439c-92a3-2ff4292a808e)

</p>
<br />

<h3>Step:11 Open IIS as an administrator 

- Click on the windows search bar and type "IIS"
- Right click the app and run as administartor 

</p>
<br />

<h3>Step:12 Register PHP Manager 

- Inside of IIS click, PHP Manager
- In "PHP setup" click Register new PHP version
  
![image](https://github.com/user-attachments/assets/0b5e0e18-f130-4d9d-a264-82d1ed3746ad)

  
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>


















