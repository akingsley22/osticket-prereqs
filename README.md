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

***NOTE*** To make sure IIS is properly installed, we can open up a web browser and enter in 127.0.0.1 (loopback) and this page to pop up.

![image](https://github.com/akingsley22/osticket-prereqs/assets/138138839/b1cdebf9-ee2a-4e01-9c03-817a890a8a5f)

Once IIS is installed, we can move on to the next step. If the installation did not work:
       
       -Go back to control panel, under programs click on unistall a program. Then click on "Turn Windows 
        features on or off". Uncheck in "Internet Information Services", click on okay and wait to uninstall.
       
       - Repeat step 2 again.
       
<p>
3.) Now that IIS is enabled, Download and Install PHP_Manager_for_IIS and Rewrite Module

4.) Create the directory C:\PHP

5.) Download PHP 7.2.8 (or the most current version) and unzip the contents into C:\PHP
     
</p>
<br />

<p>
     
![image](https://github.com/akingsley22/osticket-prereqs/assets/138138839/6296f9ad-2541-4b29-a533-f23b13e2dcb7)

</p>
<p>
6.) Download and Install VC_redist

7.) Download and Install MySQL

    -Typical Setup -> Launch Configuration Wizard (after installation)
    
    -Standard Config and install -> New root passowrd -> Execute -> Finish.

![image](https://github.com/akingsley22/osticket-prereqs/assets/138138839/be6f35bc-50a3-41c7-b3dd-c177d51b252a)

![image](https://github.com/akingsley22/osticket-prereqs/assets/138138839/a549236b-6fa9-483c-aa7e-93b6bbbb291a)

8.) Open IIS as an Admin and register PHP within IIS

      - Search for IIS in the windows search bar. Right click and select run as administrator

      -Double click on PHP Manager

      -Click on Register new PHP version

      -Click the 3 dots to browse for a path and select the php folder

      -Open up the folder and select php-cgi
      
![image](https://github.com/akingsley22/osticket-prereqs/assets/138138839/8f227d79-79d4-49fd-850b-5c267c13462f)

![image](https://github.com/akingsley22/osticket-prereqs/assets/138138839/9165b1b1-0d93-4274-bc04-43fec6519460)

***NOTE*** Make sure the file is php executable

![image](https://github.com/akingsley22/osticket-prereqs/assets/138138839/eefa26d8-20fc-4bca-9c54-098346f3c512)

9.) Restart/Reload IIS (Stop and Start the server)

![image](https://github.com/akingsley22/osticket-prereqs/assets/138138839/fbae5db7-3bfb-4ce4-a4ff-1b028f6276d8)

10.) Download osTicket (can be found in installation files)

     -Extract and copy "upload" folder into C:\inetpub\wwwroot

     -Within C:\inetpub\wwwroot, rename "upload" to "osTicket"

![image](https://github.com/akingsley22/osticket-prereqs/assets/138138839/d035a19d-0feb-4db6-8374-83d1a4b54ad6)


11.) Restart/Reload IIS again 

12.) On IIS, go to sites, then click on Default and the osTicket

     -After clicking on osTicket, click on "Browse *:80* on the right hand side of the page

![image](https://github.com/akingsley22/osticket-prereqs/assets/138138839/5c13ddca-a821-461e-8ca3-97ae5d02c191)

13.) If everything is installed correctly, you should land on this webpage

     -*Notice how some extensions are disabled. We are going to enable them in the next step.

![image](https://github.com/akingsley22/osticket-prereqs/assets/138138839/41e84325-a66f-4cf8-9d6d-ec219c136fa0)

14.) Now we are going to enable some of those disabled extensions

     -First, we go back to IIS. Click on sites -> default -> osTicket 

     -Double-click PHP Manager

     -Click "Enable or disable an extension": Enable php_imap.dll, php_intl.dll, php_opcache.dll

     -Refresh osTicket in your browser

  ![image](https://github.com/akingsley22/osticket-prereqs/assets/138138839/5085cba7-f282-474f-85bf-fe4d9243471d)

  ![image](https://github.com/akingsley22/osticket-prereqs/assets/138138839/d679f2b7-2b93-4246-b2f5-2f914bdd6d5d)

     









</p>
<br />
