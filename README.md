<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 Pro, version 22H2 - Gen2

<h2>List of Prerequisites</h2>

- Virtual Machine
- https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

<h2>Installation Steps</h2>

![vm-osticket](https://github.com/DudeOnPC/osticket-prereqs/assets/167653474/0236f036-3856-4fc1-90c9-4c9eb5b83f54)

</p>
<p>
First step for this project is to create a virtual machine to host our ticketing system.
</p>
<br />

<p>
  
![image](https://github.com/DudeOnPC/osticket-prereqs/assets/167653474/c5b32c7c-57d2-4c65-b273-3d9471895ed2)
![image](https://github.com/DudeOnPC/osticket-prereqs/assets/167653474/52b27573-a18e-47a2-aeb3-b6ee269aadc9)


</p>
<p>
In order for the installation to work properly we have to open up Control Panel--> Programs--> Turn Windows features on or off--> Check Internet Information Services(IIS) box--> Expand Application Development Features--> World Wide Web Services--> Check CGI box--> Expand Common HTTP Features and check remaining boxes that are unchecked, then click ok to finish donwloading the files for the ticketing system to work.
</p>
<br />
<p>
  
  ![image](https://github.com/DudeOnPC/osticket-prereqs/assets/167653474/224a4207-d65a-4b1b-a848-40fdf6d556c8)
  
</p>
<p>
To assure that everything was done correctly head over to 127.0.0.1 in your browser. You should see the Internet Inforamtion Services webpage. In the rare case it didn't work just uncheck the Internet Information Services box and hit ok, this will uninstall the files we downloaded and repeat the steps to reinstall the IIS files.
</p>
<br />

![image](https://github.com/DudeOnPC/osticket-prereqs/assets/167653474/5088133e-902b-41bf-8f04-c9625e35dd20)

Download PHP Manager IIS--> Download Rewrite Module--> Create a New Folder in the C: Drive named "PHP" and extract files into it--> Download VC redist.x86.exe C++ file--> Install MySQL 5.5.62--> Typical Setup--> Launch Configuration Wizard (after install)-->Standard Configuration--> Password1

![image](https://github.com/DudeOnPC/osticket-prereqs/assets/167653474/6d2a7d56-de15-4d28-a6d7-0b91dcbdc60a)
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Open IIS as an Admin

Register PHP from within IIS
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

![image](https://github.com/DudeOnPC/osticket-prereqs/assets/167653474/1306c433-6697-4e92-86c3-a8ad192b158d)

Reload IIS (Open IIS, Stop and Start the server)

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

![image](https://github.com/DudeOnPC/osticket-prereqs/assets/167653474/272d2eaf-76d4-49be-bc57-7bc4989fdb97)

Install osTicket v1.15.8
Download osTicket from the Installation Files Folder
Extract and copy “upload” folder to c:\inetpub\wwwroot
Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

![image](https://github.com/DudeOnPC/osticket-prereqs/assets/167653474/0ad519fd-d6fd-45b1-97f0-1422dc6b56f1)
Go to sites--> Default--> osTicket
On the right, click “Browse *:80”

Note that some extensions are not enabled
Go back to IIS, sites--> Default--> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browse, observe the changes

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

![image](https://github.com/DudeOnPC/osticket-prereqs/assets/167653474/a69285e1-6a44-41b1-8deb-56bcc91430fe)
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

Assign Permissions: ost-config.php
Disable inheritance--> Remove All
New Permissions--> Everyone--> All
