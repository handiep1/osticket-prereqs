<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>
<ul>
  <li>Microsoft Azure (Virtual Machines/Compute)</li>
  <li>Remote Desktop</li>
  <li>Internet Information Services (IIS)</li>
</ul>

<h2>Operating Systems Used</h2>
<ul>
  <li>Windows 10 (21H2)</li>
</ul>

<h2>List of Prerequisites</h2>
<ul>
  <li>Azure Virtual Machine</li>
  <li>Internet Information Services (IIS)</li>
  <li>PHP Manager</li>
  <li>Rewrite Module</li>
  <li>VC Redist</li>
  <li>MySQL</li>
  <li>Heidi SQL</li>
  <li>osTicket v1.15.8</li>
  <li><a href="https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">Installation files</a></li>
</ul>

<h2>Installation Steps</h2>

<p>1) First, go to Azure Portal and create a virtual machine. Choose Windows 10 Pro, version 22H2 as the OS. Make sure to select at least 2 vCPUs and 16GB of memory.</p>
<p align="center">
  <img src="https://i.imgur.com/DdSX22C.png" height="80%" width="80%" alt="Azure Portal VM creation"/>
</p>

<p>2) After creating your virtual machine, use its public IP address to connect. Open the Remote Desktop Connection app and enter the IP address to connect.</p>
<p align="center">
  <img src="https://i.imgur.com/86FVkMg.png" height="80%" width="80%" alt="Remote Desktop Connection"/>
</p>

<p>3) From now on, we'll do everything in the virtual machine. First, download the installation files for osTicket.</p>
<p align="center">
  <img src="https://i.imgur.com/KfkFZsR.png" height="80%" width="80%" alt="Downloading osTicket"/>
</p>

<p>4) After connecting to your virtual machine, open the Control Panel, go to Programs, and select Turn Windows features on or off. Then, under World Wide Web Services > Application Development Features, check the box for CGI to enable IIS with CGI.</p>
<p align="center">
  <img src="https://i.imgur.com/9M1bmJu.png" height="80%" width="80%" alt="Enable CGI in IIS"/>
</p>
  NOTE: ** Check all the boxes shown in the picture above. This will install all the necessary prerequisites for IIS on your VM.**

  <img src="https://i.imgur.com/S04VjAz.png" height="80%" width="80%" alt="Enable CGI in IIS"/>

<p>5) Once everything is installed, open a new tab and type 127.0.0.1 in the search bar. If the screen from the picture shows up, it means IIS is successfully installed on your VM.</p>
<p align="center">
  <img src="https://i.imgur.com/lByErIg.png" height="80%" width="80%" alt="Install PHP Manager"/>
</p>

<p>6)Now that IIS is enabled, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) from the installation files. Follow the install wizard to complete the installation.</p>
  <p>- Next, download and install the Rewrite Module (rewrite_amd64_en-US.msi) from the installation files.</p>
  <p> - Create a folder named "PHP" in the C drive.</p>
  <p> - Download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) from the installation files and unzip it into the C:\PHP folder.</p>

<p align="center">
  <img src="https://i.imgur.com/r5QSVBv.png" height="80%" width="80%" alt="Install PHP for osTicket"/>
  <img src="https://i.imgur.com/7zkry3i.png" height="80%" width="80%" alt="Extract osTicket"/>
  <img src="https://i.imgur.com/tbTRuBI.png" height="80%" width="80%" alt="Extract osTicket"/>

</p>

<p>7) After extracting the zip file into the C:\PHP folder, download and install VC_redist.x86.exe from the installation files. Follow the setup wizard to complete the installation.</p>

  - <p> Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi). Run the setup wizard and choose: Typical Setup -> Launch   
    Configuration Wizard -> Standard Configuration.</p>


<p align="center">
  <img src="https://i.imgur.com/kqvjAoJ.png" height="80%" width="80%" alt="Enable PHP Rewrite Module"/></p>

  - <p> After selecting Standard Configuration and setting your password, you should see a screen like this.</p>
    <img src="https://i.imgur.com/DCyg1eM.png" height="80%" width="80%" alt="Install VC Redist"/>

<p>8) Download and install the VC Redist package for the proper functioning of osTicket.</p>
<p align="center">
  <img src="https://i.imgur.com/gTfeOdZ.png" height="80%" width="80%" alt="Install VC Redist"/>
  <img src="https://i.imgur.com/tkqVDgg.png" height="80%" width="80%" alt="Install MySQL"/>

</p>

<p>9) Install MySQL to create the database for osTicket.</p>
<p align="center">
  <img src="https://i.imgur.com/yourimageid9.png" height="80%" width="80%" alt="Install MySQL"/>
</p>

<p>10) Download and install HeidiSQL for managing your MySQL database.</p>
<p align="center">
  <img src="https://i.imgur.com/yourimageid10.png" height="80%" width="80%" alt="Install HeidiSQL"/>
</p>

<p>11) Open HeidiSQL and configure the connection to your MySQL database.</p>
<p align="center">
  <img src="https://i.imgur.com/yourimageid11.png" height="80%" width="80%" alt="Configure HeidiSQL"/>
</p>

<p>12) Download the osTicket package and extract it to the correct directory in your virtual machine.</p>
<p align="center">
  <img src="https://i.imgur.com/yourimageid12.png" height="80%" width="80%" alt="Extract osTicket"/>
</p>

<p>13) Open the osTicket directory and configure the required settings for installation.</p>
<p align="center">
  <img src="https://i.imgur.com/yourimageid13.png" height="80%" width="80%" alt="Configure osTicket settings"/>
</p>

<p>14) Continue by following the osTicket installation wizard, completing all necessary steps.</p>
<p align="center">
  <img src="https://i.imgur.com/yourimageid14.png" height="80%" width="80%" alt="osTicket Installation Wizard"/>
</p>

<p>15) Finally, complete the installation and configure the osTicket settings to finish the setup process.</p>
<p align="center">
  <img src="https://i.imgur.com/yourimageid15.png" height="80%" width="80%" alt="osTicket Final Setup"/>
</p>
