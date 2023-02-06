
</p>
<br />
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

- Azure Tenant 
- Subscription
- Resourse group 
- Virtual Machine
- Virtual Network
- Subnet

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/iOHRQq4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  
<img src="https://i.imgur.com/Goxmxca.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a resource group and Virtual Machine
</p>
<br />

<p>
<img src="https://i.imgur.com/44Jfhji.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  
<img src="https://i.imgur.com/wlKglKG.png" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
While creating a virtual machine select your region inwhich you want your virtual machine to be ceated, in image select the windows 10 virtual machine with 2-4 virtual CPUs. Write  user name and pasword and remember it becuse it will use in remote desktop in upcoming step
While creating a virtual machine, allow it to create a new virtual network (Vnet)
</p>
<br />
<p>
<img src="https://i.imgur.com/rEDFJIY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now the virtual machine is created, go ahead and copy the public IP Address of the virtual machine and open the remote desktop and paste the public IP address and type the user name and password which you used while creating your virtual machine.
</p>
<br />

<p>
<img src="https://i.imgur.com/V2l4iLq.png" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
You are in side of your virtual machine, now we have to Install and enable Internet Information Services. It is a web server that run on the windows Operating System and because os ticket runs out of a website thats why we have to instal IIS. So, to do this click start and go to the control pannel>programs>turn windows features on or of. Turn on the IIS and expand it, go to the world wide web Service and expand it> then expand the application developer> CGI (because CGI let us install the PHP manager)   
</p>
<br />

<p>
<img src="https://i.imgur.com/TXymQtS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
It is the Installation File
</p>
<br />

<p>
<img src="https://i.imgur.com/lBB5ASb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the installation file download the PHP manager for IIS. 
In osTicket PHP is the back end web pragraming language.
</p>
<br />

<p>
<img src="https://i.imgur.com/GVQYnXU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the installation file download the rewrite module.
</p>
<br />

<p>
<img src="https://i.imgur.com/bByWRug.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create the directory C:\PHP. Go to the windows explorer>windows C>new folder>rename PHP. 
</p>
<br />

<p>
<img src="https://i.imgur.com/EX2RTvA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the Installation file download PHP 7.3.8 and unzip the content into C:\PHP.
Extract all>browse>this PC>windows C>PHP>select folder>Extract.
</p>
<br />

<p>
<img src="https://i.imgur.com/XGawRaH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the installation file download VC redistX86.exe.
</p>
<br />

<p>
<img src="https://i.imgur.com/dFSffoX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/Q3MpuUD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the Installation file download MYSQL.5.5.62.
  
Open it and agree. Select the typical setup and install. Make sure that the box is marked before Installing.
  
Select the standard configuration> user name is root and password is Password1> execute>finish.
</p>
<br />

<p>
<img src="https://i.imgur.com/ZF4QNX9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open IIS as administrator
</p>
<br />

<p>
<img src="https://i.imgur.com/UdjtoZd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/JRxIs2M.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Register PHP from within IIS and to do that go to PHP manager>register new PHP version>click the --- on the right>C drive>PHP>Php-cgi>ok.
</p>
<br />

<p>
<img src="https://i.imgur.com/vxkHX7l.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Reload the IIS. Select to the vmosTicket and click restart.
</p>
<br />

<p>
<img src="https://i.imgur.com/gBIAb3e.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/2MWizjq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download the osTicket from the Installation file folder.Extract and copy “upload” folder to c:\inetpub\wwwroot
Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”

  
Open file explorer next to each other. Go to the download and drag upload folder into c:\inetpub\wwwroot and let it install and then rename the name of upload folder to osTicket.
</p>
<br />

<p>
<img src="https://i.imgur.com/nsSdVnB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Reload the IIS again and then go to sites>Default>osTicket
  
On the right click Browse 80
</p>
<br />

<p>
<img src="https://i.imgur.com/gJ6ChZw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
If you can see this page which means you are good so far.
</p>
<br />

<p>
<img src="https://i.imgur.com/8GkvB1V.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go back to the IIS>sites>Default>osTicket. Double click the PHP manager>enable or disable extension. We have to enable these extensions.
  
Enable: php_imap.dll
  
  
Enable: php_intl.dll
  
  
Enable: php_opcache.dll
  
Refresh the osTicket site in your browser and observe the changes.

</p>
<br />

<p>
<img src="https://i.imgur.com/4D0VxDz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Rename ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php>rename

  
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

  
</p>
<br />

<p>
<img src="https://i.imgur.com/C6RSD86.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Assign permission to ost-config.php, go to properties>security and disable inheritance>remove all. New permission to everyone.
</p>
<br />

<p>
<img src="https://i.imgur.com/Zazf1ee.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Click countinue in the osTicket browser to countinue settings.
  
Name Helpdesk (Kanza’s Help Desk)
  
  
Default email (receives email from customers)kanza@helper.com
  
Set user name and password and rember it to login in future. In this case user name is Kanza.

  
</p>
<br />

<p>
<img src="https://i.imgur.com/7dmR4Sm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and Install the HeidiSQL from the Installation folder
</p>
<br />

<p>
<img src="https://i.imgur.com/zW70gAl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Create a new session, root with the Password1 and connect to it.
  
</p>
<br />

<p>
<img src="https://i.imgur.com/CUqRk6b.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a new data bese called osTicket.
  
Right click to the unnamed>create new>database> name it osTicket.
</p>
<br />

<p>
<img src="https://i.imgur.com/n16FZht.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to the osTicket page and type root in MYSQL username, Password1 in MYSQL Password, and osTicket in MYSQL Database and click to Install now.
  
</p>
<br />

<p>
<img src="https://i.imgur.com/QGiGVax.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Congratulations, Your setup is complted successfully
  
</p>
<br />

<p>
<img src="https://i.imgur.com/DLXS1uV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
But first we have to cleanup some thing.
  

Delete the setup folder. Go to C:\inetpub\wwwroot\osTicket\setup.
  
  
</p>
<br />

<p>
<img src="https://i.imgur.com/XSQXcZW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Go to C:\inetpub\wwwroot\osTicket\include\ost-config.php>properties>securiery>advanced>everyone>EDIT>and unchecked everything and just leave it to read and execute.

  
</p>
<br />

<p>
<img src="https://i.imgur.com/h4JSwCL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now you can login with your user name and password that you created while setting up your admin user. In my case it is kanza with Password1.
</p>
<br />

<p>
<img src="https://i.imgur.com/GqfFjze.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Congratulation, You are inside of your osTicket setup.
</p>
<br />


