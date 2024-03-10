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

- Azure Virtual Machine
- Internet Information Services (IIS)
- PHP Manager
- Rewrite Module
- VC Redist
- MySQL
- Heidi SQL
- osTicket v1.15.8
- Files needed for osTicket Installation https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6


<h2>Installation Steps</h2>
<h3>1. Create a resource group and a virtual machine in azure </h3>
<ul>
  <li>Go to https://portal.azure.com/ and sign in</li>
  <li>Choose or create a resource group</li>
  <li>Create a Window 10 Virtual Machine (VM) with 2-4 virtual CPUs</li>
  <li>Set the desired name for the virtual machine</li>
  <li>Create Username/Password</li>
</ul>

<h3>2. Install/Enable IIS on Windows with CGI and Common HTTP Features enabled</h3>
<p> + In Windows Virtual Machine (VM), go to Control Panel > Programs > Programs & Features, and Turn Windows features on and off</p>
<ul>
  <li> Check the box Internet Information Services </li>
  <li>Expand the list for Internet Information Services, navigate to World Wide Web Services then expand that to find Application Development Features, expand that and check the box for CGI.</li>
  <li>Before closing, make sure the boxes under Common HTTP Features in World Wide Web Services are checked.</li>
</ul>


<p>
<img src="https://i.imgur.com/dHKLmT4.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/rjR4ftB.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
<li>Confirm that everything is set up correctly. Go to the browser on VM and type in 127.0.0.1. It should load Internet Information Services.</li>
</p>
<img src="https://i.imgur.com/0NoXMmJ.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />


<p>
<h3>3. Install PHP Manager for IIS</h3>
  <ul>
    <li>Download "PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)" from the installation files.</li>
    <li>Run the installer and follow the on-screen instructions to complete the installation.</li>
  </ul>
<img src="https://i.imgur.com/aw5LWgC.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />



<p>
  <h3>4. Install Rewrite Module</h3>
  <ul>
    <li>Download "Rewrite Module (rewrite_amd64_en-US.msi)" from the installation files.</li>
    <li>Run the installer and follow the on-screen instructions to complete the installation.</li>
  </ul>
<img src="https://i.imgur.com/7VxO3Y5.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<h3>5. Create Directory for PHP </h3>
<li>Create a directory C:\PHP.</li>
<li>Download PHP 7.3.8 and unzip its contents into C:\PHP</li>
<li>If prompted, choose to keep the file</li>
<img src="https://i.imgur.com/B2EESJF.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
<h3>6. Install VC_redist.x86.exe </h3>
  <li>Download and install "VC_redist.x86.exe" from the installation files.</li>
<img src="https://i.imgur.com/Qq84XiA.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
<h3>7. Install MySQL 5.5.62</h3>
  <ul>
    <li>Download "MySQL 5.5.62 (mysql-5.5.62-win32.msi)" from the installation files.</li>
    <li>Run the installer, choose "Typical Setup", and follow the prompts.</li>
    <li>Launch Configuration Wizard after install, choose "Standard Configuration", set the root password</li>
  </ul>
<img src="https://i.imgur.com/Uj77jod.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />


<p>
<h3>8. Register PHP in IIS</h3>
<img src="https://i.imgur.com/7iFk64U.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br/>
<li>Open IIS as an admin</li>
<img src="https://i.imgur.com/TC6tPyJ.png" height="50%" width="50%" alt="Disk Sanitization Steps"/> 

<li> Register PHP from within IIS</li>
<img src="https://i.imgur.com/3pxxYvn.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
<h3>9. Reload IIS</h3>
  <li>Stop and start the IIS server.</li>
<img src="https://i.imgur.com/Ga7qmco.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
<h3>10. Install os ticket v1.15.8</h3>
  <ul>
    <li>Download osTicket from the Installation Files Folder.</li>
    <li>Extract and copy the "upload" folder to "C:\inetpub\wwwroot".</li>
    <li>Rename the "upload" folder to "osTicket" within "C:\inetpub\wwwroot".</li>
  </ul>
<img src="https://i.imgur.com/lfWHQ7Y.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
<h3>11.Reload IIS Again/Configure osTicket in IIS</h3>
  <ul>
    <li>Go to sites -> Default -> osTicket.</li>
    <li>On the right, click "Browse *:80".</li>
  </ul>
<img src="https://i.imgur.com/Ga7qmco.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
<h3>12. Enable PHP Extensions </h3>
  <ul>
    <li>Go back to IIS, sites -> Default -> osTicket.</li>
    <li>Double-click PHP Manager.</li>
    <li>Click "Enable or disable an extension".</li>
    <li>Enable: php_imap.dll, php_intl.dll, php_opcache.dll.</li>
  </ul>
<img src="https://i.imgur.com/jybnWSr.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
<h3>13. Rename and Assign Permissions to ost-config.php </h3>
  <ul>
    <li>Rename: ost-config.php from "C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php" to 
    "C:\inetpub\wwwroot\osTicket\include\ost-config.php".</li>
    <img src="https://i.imgur.com/HJ2nCZe.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
    <li>Disable inheritance, remove all permissions, then assign Everyone with all permissions.</li>
  </ul>
<img src="https://i.imgur.com/tATCuj0.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/NkvHQDx.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />



<p>
<h3>14. Continue Setting up osTicket in the browser </h3>
  <ul>
    <li>Navigate to the osTicket installation page.</li>
    <li>Provide necessary details like Helpdesk name, default email, etc.</li>
    <li>Continue with the setup process.</li>
  </ul>
<img src="https://i.imgur.com/s1FXmvh.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
<h3>15. Install HeidiSQL </h3>
  <ul>
    <li>Download and install HeidiSQL from the installation files.</li>
    <img src="https://i.imgur.com/grI1VyV.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
    <li>Open HeidiSQL and create a new session.</li>
    <li>Connect to the session and create a database called "osTicket".</li>
  </ul>
<img src="https://i.imgur.com/rdCIO4h.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
<h3>16. Continue Setting up osTicket in the browser </h3>
  <ul>
    <li>Provide MySQL database, username, and password details.</li>
    <li>Click "Install Now!" to complete the setup.</li>
  </ul>
<img src="https://i.imgur.com/DO7foG9.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
<h3> CONGRATULATIONS! </h3>
<li>Verify the installation by browsing to the help desk login page</li>
<img src="https://i.imgur.com/44dxRXx.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>

<h3>DON'T FORGET CLEAN UP</h3>
<li>Delete: C:\inetpub\wwwroot\osTicket\setup</li>
<li>Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php</li>
