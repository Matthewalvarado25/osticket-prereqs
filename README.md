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
-  Use Remote Desktop Protocal in the VM
-  Download osticket instalation files within the virtual machine
-  Enable IIS in Windows with CGI
-  Download and install PHP manager for IIS 
-  Download and install the Rewrite Module
-  Create the directory C:\PHP
-  Download PHP 7.3.8 and unzip the contents into C:\PHP
-  Download and install VC_redistx86 
-  Download and install MYSQL 5.5.62
-  Open IIS as an Admin and register PHP from within IIS
-  Made osTicket v1.15.8
-  Download and install HeidiSQL
-  Finish up osTicket in the browser
<h2>Installation Steps</h2>
<h3>Step:1 Create a Virtual Machine(VM) in Azure</h3>

<p>
  
- Create a resource group in Azure
- Create a virtual machine
    - In Image, select Windows 10 Pro version 22H2
    - In Size, select option with at least 2 vcpus
    - Create a username and password for your account
    - Review and create
</p>
<br/>

<h3>Step:2 Create a Virtual Machine(VM) in Azure</h3>

- Locate your VM's public IP address and copy it
- Open the Microsoft remote desktop app
- Then paste the virtual machine's public IP address inside the text field
  
![image](https://github.com/user-attachments/assets/50da2c37-18cd-4593-9467-0658d6d7a1ea) ![image](https://github.com/user-attachments/assets/f08829e2-05bb-4905-ba55-5f43db334036)

</p>
<br/>

<h3>Step:3 Download the osticket instalation files</h3>
  
- Copy the osticket files link, then inside the VM open the browser, paste a link inside the search bar, and download the files


</p>
<br/>

<h3>Step:4 Enable IIS</h3>

- Look up "control panel" on the search bar
- Open the control panel and select programs
- Click on "Turn Windows features on or off"
- Browse to approve and expand "Internet Information Services(IIS)"
- Approve and expand "World Wide Web Services"
- Expand "Application Development Features"
- Approve CGI then hit "Ok"
  
  ![image](https://github.com/user-attachments/assets/8a271ebb-0905-4eb3-a677-894c4582347d)

</p>
<br/>

<h3>Step:5 Download PHP Manager</h3> 
  
- Install PHPManagerForIIS_V1.5.0.msi from the osTicket-Installation-Files folder 
  
</p>
<br/>

<h3>Step:6 Download Rewrite Module</h3> 

- Install rewrite_amd64_en-US.msi from the osTicket-Installation-Files folder 

</p>
<br/>

<h3>Step:7 Create a new Directory</h3>

- Open file explorer
- Click on "this PC"
- Navigate to the windows (C:)Drive
- In the Windows (C:) Drive, create a new folder titled "PHP"

</p>
<br/>

![image](https://github.com/user-attachments/assets/cabc0581-b7f5-495b-b93b-70a44d5881e9)


</p>
<p>
  
<h3>Step:8 Extract php-7.3.8-nts-Win32-VC15-x86.zip</h3>

  
</p>

- Find, php-7.3.8-nts-Win32-VC15-x86.zip folder in downloaded osTicket Installation Files
- Right click on the folder and choose extract all, then select the PHP folder from the (C:) Drive

![image](https://github.com/user-attachments/assets/97fa47e5-ddfa-4ba9-ab77-3a0c7bc282e0)

  
</p>
<br/>

<h3>Step:9 Install VC_redist.x86.exe</h3>
  
</p>

- Install VC_redist.x86.exe from the osticket installation files
  
<p>
  
</p>
<br/>

<h3>Step:10 Install MySQL 5.5.62</h3>
  
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

<h3>Step:11 Open IIS as an administrator</h3> 

- Click on the windows search bar and type IIS
- Right click the app and run as administartor 

</p>
<br />

<h3>Step:12 Register PHP Manager</h3>

- Inside of IIS click, PHP Manager
- In PHP setup, click Register new PHP version
  
![image](https://github.com/user-attachments/assets/0b5e0e18-f130-4d9d-a264-82d1ed3746ad)

- After clicking Register new PHP version, you will be required to provide a path to php-cgi.exe
- You will click the 3 dots to the right to open file explorer
- Navigate to the Windows (C:) Drive, Folder PHP, select php-cgi -> click Ok

</p>

  
![image](https://github.com/user-attachments/assets/f6dd14fd-9378-4e44-b651-bba92260e5f2)

</p>
<br />

<h3>Step:13 Restart IIS</h3>

- Inside of IIS click, osticket-vm on the top left, under connections
- Right click on osticket-vm and stop it, then start it back up after a second to restart the web server

![image](https://github.com/user-attachments/assets/e1942b65-2df6-47d7-88a5-57d0509e3b4c)

</p>
<br />

<h3>Step:14 Install osTicket</h3>

- Extract files in osTicket-v1.15.8 folder
- Next open a new File Explorer window
- Within the new File Explorer window, scroll to the Windows (C:) Drive -> inetpub -> wwwroot
- Drag the "Upload" folder from the extracted files into the wwwroot folder
- Lastly rename the Upload folder to osTicket

![image](https://github.com/user-attachments/assets/d17683d4-c36d-47d5-8ceb-e2772d101718)

</p>
<br />

<h3>Step:15 Restart IIS again</h3>
  
- Go back into IIS
- Follow the same steps as you you did in Step:13

</p>
<br />

<h3>Step:16 Load the osTicket site</h3>
  
- Inside IIS, expand the Sites dropdown -> expand Default Web Site -> click osTicket
- On the right side of the window, click on Browse *80 (http)
- The osTicket site should load 

![image](https://github.com/user-attachments/assets/5fd3cff2-5bce-4625-a53d-7315b2fe9d14)
<p>
  
![image](https://github.com/user-attachments/assets/b09c2a09-f6a5-41c9-b91d-33ef23ed14f2)


</p>
<br />

<h3>Step:17 Enable Extensions</h3>
  
- Go back into IIS
- On the left side of window, expand Sites folder -> click Default Web Site -> click on osTicket folder
- Click on PHP Manager
- Click Enable or disable an extension link under, PHP Extensions
- Enable the following extenstions:
  php_imap.dll ,
  php_intl.dll ,
  php_opcache.dll 

<p>

  
![image](https://github.com/user-attachments/assets/3fb3e765-b7f2-4ed7-a545-6c6235b959bd)

<p>
  
![image](https://github.com/user-attachments/assets/76f9d048-5da6-4023-959b-6f9164a84a11)

<p>

  
![image](https://github.com/user-attachments/assets/64bb22e4-29eb-4e30-9e68-d93f0a243080)


- Refresh the osTicket website in your browser and you will see that the previously disabled features are now enabled

![image](https://github.com/user-attachments/assets/5515aac3-6493-4178-9c71-fee4a025d2b9)



</p>
<br />


<h3>Step:18 Rename ost-config.php</h3>
  
- Open File Explorer and navigate to Windows (C:) Drive -> inetpub -> wwwroot -> osTicket -> include
- Inside the "include" folder, locate "ost-sampleconfig.php" file
- Rename ost-sampleconfig.php file to ost-config.php


</p>
<br />

<h3>Step:19 Assign Permissions in "ost-config.php"</h3>
  
- Right click on "ost-config.php" file and click properties
- We want to enable anyone to edit the file.
- Select secruity then advance and disable all inheritance.
- Next click add and click add properties.
- Type in "everyone" in the section and hit apply then ok and now everyone can edit!
  
![image](https://github.com/user-attachments/assets/56fb35a3-7643-4e13-9c66-03d505e74b4b)


<p>

  
![image](https://github.com/user-attachments/assets/47513092-a2c3-45b2-b861-3f018718495d)

</p>
<br />

<h3>Step:20 Continue osTicket setup</h3>
  
- Inside the osTicket webpage, click "Continue"
- Fill out "System Settings" and "Admin User"
- The two email addresses for email admin and email user should be different

</p>
<br />

<h3>Step:21 Install HeidiSQL"</h3>
  
- Install "HeidiSQL_12.3.0.6589_Setup" from downloaded osTicket Installation Files
- Open HeidiSQL
- Click "New" at bottom left of window to create a new session
- In the new session the user name will be "root" and you will also need to create a password
- Click "Open" to connect to session database
- on the top left, right click on "Unnamed" -> create new -> Database
- create a database and name it "osTicket", then click "Ok"

![image](https://github.com/user-attachments/assets/a8450275-a694-43ef-8108-d6593d3077b7)

</p>
<br />

<h3>Step:22 Finish osTicket system</h3>
  
- Finish setting up osTicket, by filling out the "database settings"
- Then click "Install Now" and osTicket will be installed

![image](https://github.com/user-attachments/assets/8a958b78-cedc-449a-a12c-c791dbd97d9c)

</p>
<br />

![image](https://github.com/user-attachments/assets/2d86362f-e961-4e34-a302-a1162dc3fe83)

<h3> You have succesfully made osTicket. Congratulations!!!

