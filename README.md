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


Download PHP Manager IIS--> Download Rewrite Module--> Create a New Folder in the C: Drive and call it "PHP"

