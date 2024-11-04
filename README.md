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

- Microsoft Azure
- Windows Virtual Machine
- IIS in Windows (with CGI) must be enabled/installed
- PHP Manager
- Rewrite Module
- VC_redist
- MySQL 5.5.62
- Heidi SQL
- osTicket
- You can download all the necessary files here https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD

<h2>Installation Steps</h2>

<p>
In Microsoft Azure create a Virtual Machine, make sure the image is "Windows 10" and the size is at least 2 vcpus with 8 GB of memory.

Then use "Remote Desktop" to connect to your virtual machine.
</p>
<p>
<img src="https://i.imgur.com/oaL1sne.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/WVZRw5u.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/DSgwEfj.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Once inside your virtual machine download the  “osTicket-Installation-Files” folder and unzip the folder onto your desktop.
</p>
<p>
<img src="https://i.imgur.com/WEoUs2S.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/yL1K4Fu.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
From the start menu, type "control panel" in the search box and hit enter. 
  
Open the control panel and navigate to "programs", then "Turn Windows features on or off". 

Once in Windows features click on "Internet information services" > "World Wide Web Services" > "Application Development Features", then check the box named "CGI".
</p>
<p>
<img src="https://i.imgur.com/LtGJsxQ.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/QmFdcQ6.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
From the Installation folder, install PHP Manager
</p>
<p>
<img src="https://i.imgur.com/g3IdgYM.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/zIfeeAw.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
From the Installation folder, install the Rewrite Module
</p>
<p>
<img src="https://i.imgur.com/zvXwekC.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/OUhqKXI.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />

<p>
Create a new folder in the C: drive and name it PHP.

Then, From the Installation folder, unzip "php-7.3.8-nts-Win32-VC15-x86.zip" into the new PHP folder we just created.
</p>
<p>
<img src="https://i.imgur.com/u5JM4Gp.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/t45UZ5p.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/AqPtSLZ.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
  
<p>
From the installation folder, install Vc_redist.x86
</p>
<p>
<img src="https://i.imgur.com/i5PPBCw.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/IIaiDfZ.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>  
<br />

<p>
From the Installation folder, install MySQL using the following settings.

Typical Setup 

Launch Configuration Wizard  > Standard Configuration > Install as Windows Service

Make the Username and Password "root"
</p>
<p>
<img src="https://i.imgur.com/rl0acRX.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/vd8xHvE.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/erm7Uc0.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/6Gw67w8.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/zW55opw.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/cEFCO3C.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/TtmnYtM.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />

<p>
Open IIS as an Admin (start > search > IIS > IIS manager) 
  
Register PHP from within IIS (PHP Manager > C:\PHP\php-cgi.exe)

Then reload the IIS by clicking "Stop" then "Start"
</p>
<p>
<img src="https://i.imgur.com/7sMXSzG.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/ARDawFA.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/zwMe1t1.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/bdJiYXC.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />

<p>
From the installation folder unzip the “osTicket-v1.15.8.zip” folder to the desktop. 
  
Then from the desktop, copy the “upload” folder into “c:\inetpub\wwwroot” and Rename “upload” to “osTicket”.

Then Reload the IIS again (Open IIS, Stop and Start the server).
</p>
<p>
<img src="https://i.imgur.com/VCwsqVc.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/5vMMz8n.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/IJXrpVV.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/D1ZrKFs.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />

<p>
While in IIS navigate to "sites" > "Default Web Site" > "osTicket"

Then On the right, click “Browse *:80”

Now, we notice that some extensions are not enabled so we need to go back to IIS and enable them.

Go back to IIS, "sites" > "Default Web Site" > "osTicket" > "PHP Manager" > “Enable or disable an extension”

Now from here we will search for and enable the following extensions.

Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll

Now we can go back and refresh the osTicket site in our browser and see that the extensions are now enabled.


</p>
<p>
<img src="https://i.imgur.com/aP63bTN.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/Z8exokZ.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/KmFXQpw.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/z6mlGsN.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/yq8rwjI.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/2cXlv05.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/GdvlP0L.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/sKPmFJl.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />

<p>
Next, we will go to our osTicket directory inside c:\inetpud\wwwroot\osTicket

Navigate to the folder named "include" then find the file named "ost-sampleconfig.php" and change the file name to "ost-config.php"

Now we need to assign permissions for this file.

Right-click the file and select "properties" then "advanced" > "Disable inheritance" > "Remove All"

Go back to "properties" > "edit" > "add"

Now we can type "Everyone" in the box and select "ok" (tip: you can click "check names" to make sure that the user or group name you typed in exists).

Finally, make sure to allow "everyone" to have all permissions (simply check the "full control" box).
</p>
<p>
<img src="https://i.imgur.com/3bZ4c4k.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/dHVZG1j.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/p9CxPmw.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/k5lVNwp.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />

<p>
The next step is to continue setting up osTicket in the browser by clicking continue.

Fill out the text fields but stop when you reach the "database settings" section. 
</p>
<p>
<img src="https://i.imgur.com/85NcHID.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />

<p>
From the installation folder, install HeidiSQL and run it.

Once in Heidi SQL, create a new session using "root" for the username and password, and open the connection.

Right-click in the white area and select "create new" then "database" and name it "osTicket".
</p>
<p>
<img src="https://i.imgur.com/veNSmBJ.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/Meu9TCB.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/bx68ihn.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/1t1GgP5.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/xbjavPp.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />

<p>
Go back to osTicket in the browser and finish filling out the page using the following information.

MySQL Database: osTicket
 
MySQL Username: root

MySQL Password: root

Now click "install" and you should be directed to the confirmation page.

</p>
<p>
<img src="https://i.imgur.com/Ry28azs.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/eLr2kEs.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />

<p>

Now you can browse to your help desk login page: http://localhost/osTicket/scp/login.php

</p>
<p>
<img src="https://i.imgur.com/Xzq7U0S.jpeg" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<br />
<p>

<h2>Congratulations!!</h2>
You've successfully installed osTicket and all its prerequisites.
</p>
<p>
<img src="https://i.imgur.com/1hI4Zv6.gif" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<br />
