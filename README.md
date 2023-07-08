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


- Microsoft Azure Virtual Machine
- Install IIS in Windows and enable CGI and HTTP Features
- PHP_Manager_for_IIS
- Rewrite Module
- VC Redist
- MySQL
- Heidi SQL
- Latest version of PHP
- Latest version of osTicket
- Link with all downloadable prerequisites: https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

<h2>Installation Steps</h2>

1.) To begin, we must first create a virtual machine withine the Microsoft azure portal. For this demonstration, the VM will be ran on a Windows 10 server with 2 vcpus and 16 GiB memory.

Once VM is created, connect to it using Remote Desktop Connection. We will connect using the public IP address that can be found in the overview section of the VM.

![image](https://github.com/akingsley22/osticket-prereqs/assets/138138839/0f27a8ef-f794-4ee8-9e1b-e5018ce4323b)


<p>
2.) After connecting successfully to the server, the next step is Installing IIS on windows and enabling CGI and HTTP Features. IIS is a web server that allows the computer serve up websites and because osTicekt runs out of a website, we need to set up and configure IIS.
     
     -First step in doing this is double clicking on the programs setting in the control panel. Then click on "Turn Windows 
      features on or off".
      
     - Next enable CGI (under Application Development Features) and all Common HTTP features
  
</p>
<br />

<p>

![image](https://github.com/akingsley22/osticket-prereqs/assets/138138839/830d376d-2e9a-4825-a422-4d80becc72dd)

</p>

NOTE! To make sure IIS is properly installed, we can open up a web browser and enter in 127.0.0.1 (loopback) and this page to pop up.

![image](https://github.com/akingsley22/osticket-prereqs/assets/138138839/b1cdebf9-ee2a-4e01-9c03-817a890a8a5f)

Once IIS is installed, we can move on to the next step. If the installation did not work:
       -Go back to control panel, under programs click on unistall a program. Then click on "Turn Windows 
      features on or off". Uncheck in "Internet Information Services", click on okay and wait to uninstall.
       - Repeat step 2 again.
       
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
3.) 
</p>
<br />
