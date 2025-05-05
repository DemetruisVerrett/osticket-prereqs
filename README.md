<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [ClipChamp: How To Install osTicket with Prerequisites](https://1drv.ms/v/c/5dac4edc6b620d54/EVp75XjxqfFDpNtROIv56CgBtBB0w9x_YFm18g4scVjIxQ)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Microsoft Azure account
- Virtual Machines
- Remote Desktop
- osTicket installation files
- SQL

<h2>Installation Steps</h2>

<p>
 
![Image](https://github.com/user-attachments/assets/52544ced-0682-4578-ab94-863cab5a887e)

</p>
<p>
 1. Create Azure Virtual Machine:
Name: osticket-vm
 
Username: labuser

Password: osTicketPassword1!

Size: 4 vCPUs (Windows 10 Pro)

2. Log into VM via Remote Desktop:Use the provided username and password to connect to the VM.
3. Prepare VM for osTicket Installation:Download osTicket Files: Download osTicket-Installation-Files.zip and unzip it on the desktop into a folder called osTicket-Installation-Files.
4. Enable IIS with CGI Support:
Go to Control Panel > Programs and Features > Turn Windows Features On/Off.
Enable IIS with CGI under World Wide Web Services > Application Development Features.

5. Install Dependencies:
PHP Manager for IIS: Install PHPManagerForIIS_V1.5.0.msi from the folder.

URL Rewrite Module: Install rewrite_amd64_en-US.msi from the folder.

PHP: Create C:\PHP and unzip php-7.3.8-nts-Win32-VC15-x86.zip into it.

VC Redistributable: Install VC_redist.x86.exe.

MySQL 5.5.62: Install mysql-5.5.62-win32.msi with Typical Setup. 

Configure MySQL with:

Username: root

Password: root

After these steps, your VM will be set up with IIS, PHP, and MySQL, ready to install osTicket.




</p>
<br />

<p>
 
 ![Image](https://github.com/user-attachments/assets/a6cb4e2f-ae70-46b6-b3fc-440dba6d5af3)

</p>
<p>
1. Register PHP in IIS:
Open IIS as Administrator.

Register PHP:
Open PHP Manager in IIS.
Register PHP by selecting C:\PHP\php-cgi.exe.Reload IIS:

Open IIS Manager.
Stop and Start the server to apply changes.

2. Install osTicket v1.15.8:
Extract osTicket Files:

From the osTicket-Installation-Files folder, unzip osTicket-v1.15.8.zip.
Copy the upload folder into C:\inetpub\wwwroot.
Rename upload to osTicket.
Reload IIS:

Stop and start the IIS server again to apply changes.

3. Access osTicket:
Go to Sites > Default > osTicket in IIS.
Click *Browse :80 to open the osTicket site in your browser.

4. Enable Required PHP Extensions:
In IIS, go to Sites > Default > osTicket.
Double-click PHP Manager.
Click Enable or disable an extension.
Enable the following PHP extensions:
php_imap.dll
php_intl.dll
php_opcache.dll
Refresh the osTicket site in the browser to see the changes.

5. Configure osTicket:
Rename ost-sampleconfig.php:

Go to C:\inetpub\wwwroot\osTicket\include.
Rename ost-sampleconfig.php to ost-config.php.
Assign Permissions to ost-config.php:

Right-click ost-config.php, go to Properties > Security.
Disable inheritance and Remove all permissions.
Add Everyone and give Full Control.

This sets up osTicket, ensures required extensions are enabled, and configures permissions for the ost-config.php file.
</p>
<br />

<p>
 
![Image](https://github.com/user-attachments/assets/3832d088-91a8-482c-9a76-2cd38d24be7a)

</p>
<p>
1. Continue osTicket Setup in the Browser:
Click Continue to proceed.
Helpdesk Name: Enter a name for your helpdesk.
Default Email: Set the email address that will receive customer emails.

 2. Install HeidiSQL (Database Management):
From the osTicket-Installation-Files folder, install HeidiSQL.
Open HeidiSQL, create a new session with:

Username: root

Password: root

Connect to the MySQL session.

3. Create Database in HeidiSQL:
In HeidiSQL, create a new database called osTicket.

4. Complete osTicket Installation in Browser:
In the osTicket web installer:
MySQL Database: osTicket

MySQL Username: root

MySQL Password: root

Click Install Now! to complete the installation.

6. Final Setup:
Once installation is successful, browse to the Help Desk Login Page:
http://localhost/osTicket/scp/login.php

End Users osTicket URL:
http://localhost/osTicket/

This completes the installation and setup of osTicket on your VM.
</p>
<br />
