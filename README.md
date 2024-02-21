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
<p><h3>1. Create a resource group and a virtual machine in azure </h3></p>
<ul>
  <li>Go to https://portal.azure.com/ and sign in</li>
  <li>Choose or create a resource group</li>
  <li>Create a Window 10 Virtual Machine (VM) with 2-4 virtual CPUs</li>
  <li>Set the desired name for the virtual machine</li>
  <li>Create Username/Password</li>
</ul>

<p><h3>2. Install/Enable IIS on Windows with CGI and Common HTTP Features enabled</h3></p>
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
<img src="https://i.imgur.com/aw5LWgC.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />



<p>
  <h3>4. Install Rewrite Module</h3>
<img src="https://i.imgur.com/7VxO3Y5.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<h3>5. Setup PHP </h3>
<li>Create a directory at C:\PHP.</li>
<img src="https://i.imgur.com/B2EESJF.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<li>Download PHP 7.3.8 and unzip its contents into C:\PHP</li>
<li>If prompted, choose to keep the file</li>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<h3>6. Install VC_redist.x86.exe </h3>
<img src="https://i.imgur.com/Qq84XiA.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<h3>7. Install MySQL 5.5.62</h3>
<img src="https://i.imgur.com/Uj77jod.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
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
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<h3>9. Reload IIS</h3>
<img src="https://i.imgur.com/Ga7qmco.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<h3>10. Install os ticket v1.15.8</h3>
<img src="https://i.imgur.com/lfWHQ7Y.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<h3>11.Reload IIS Again</h3>
<img src="https://i.imgur.com/Ga7qmco.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<h3>12. Configure PHP Extensions </h3>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<h3>13. Rename ost-config.php</h3>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<h3>14. Assign Permissions </h3>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<h3>15. Continue Setting up osTicket in the browser </h3>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<h3>16. Install HeidiSQL </h3>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<h3>17. Continue Setting up osTicket in the browser </h3>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />



<h3> CONGRATULATIONS! </h3>
<img src="https://i.imgur.com/44dxRXx.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<li>Verify the installation by browsing to the help desk login page</li>
