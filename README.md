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

<p>8) Next, click the Windows icon, type "IIS," right-click it, and select "Run as administrator." The last picture shows all the prerequisites you installed.</p>
<p align="center">
  <img src="https://i.imgur.com/gTfeOdZ.png" height="80%" width="80%" alt="Install VC Redist"/>
  <img src="https://i.imgur.com/tkqVDgg.png" height="80%" width="80%" alt="Install MySQL"/>

</p>

<p>9) We will now want to register PHP from within IIS. Click on PHP Manager. </p>
<p align="center">
  <img src="https://i.imgur.com/AUuQ9qY.png" height="80%" width="80%" alt="Install MySQL"/></p>
  
  - <p> Now, register PHP in IIS by clicking on PHP Manager. </p>
    <img src="https://i.imgur.com/6WTpnv9.png" height="80%" width="80%" alt="Install HeidiSQL"/>


<p>10) Click on PHP Manager and select "Register new PHP version." Browse to the C drive, open the PHP folder, select php.cgi, and click "Open," then "OK." Finally, restart IIS from the home screen to ensure everything is ready for osTicket.</p>
<p align="center">
  <img src="https://i.imgur.com/IXA9cW0.png" height="80%" width="80%" alt="Install HeidiSQL"/>
</p>

<p>11) Open two file folders: one from the Downloads section and one from the C drive. In the C drive, go to Inetpub > wwwroot, then move the "upload" folder from the osTicket download folder into wwwroot. Rename the "upload" folder to "osTicket."</p>
<p align="center">
  <img src="https://i.imgur.com/IVGLg6c.png" height="80%" width="80%" alt="Configure HeidiSQL"/>
  <img src="https://i.imgur.com/qSmDDdV.png" height="80%" width="80%" alt="Configure HeidiSQL"/>
  <img src="https://i.imgur.com/Wqrlebs.png" height="80%" width="80%" alt="Configure HeidiSQL"/>
  <img src="https://i.imgur.com/UdjTEet.png" height="80%" width="80%" alt="Extract osTicket"/>
</p>

<p>12) On IIS go to sites -> Default -> osTicket -On the right, click “Browse *:80”.</p>
<p align="center">
  <img src="https://i.imgur.com/INaYr32.png" height="80%" width="80%" alt="Extract osTicket"/>
    -<p> Once you press the button browse *:80(http) you should see a tab open that has the picture posted below. </p>
    <img src="https://i.imgur.com/6uB9Vnu.png" height="80%" width="80%" alt="Configure osTicket settings"/></p>
</p>

<p>13) Go to IIS > Default > osTicket, then double-click PHP Manager. Click "Enable or Disable Extensions" and enable php_imap.dll, php_intl.dll, and php_opcache.dll. After that, refresh the osTicket site in the browser, and the red X's should turn green.</p>
<p align="center">
  <img src="https://i.imgur.com/8YL4O94.png" height="80%" width="80%" alt="Configure osTicket settings"/>
  <img src="https://i.imgur.com/Xq69wsp.png" height="80%" width="80%" alt="Configure osTicket settings"/>
  <img src="https://i.imgur.com/bgIDTXz.png" height="80%" width="80%" alt="Configure osTicket settings"/>

</p>

<p>14)After enabling the extensions, go to C:\inetpub\wwwroot\osTicket\include\ in File Explorer and find ost-sampleconfig.php.</p>
<p align="center">
    -<p> Rename ost-sampleconfig.php to ost-config.php. </p>
  <img src="https://i.imgur.com/xyOV5G5.png" height="80%" width="80%" alt="osTicket Installation Wizard"/>
  <img src="https://i.imgur.com/brrFGAX.png" height="80%" width="80%" alt="osTicket Installation Wizard"/>

  -<p> Right-click the file, select Properties, then go to the Security tab. Click Advanced, disable inheritance, and choose   "Remove all inherited permissions." </p>

  <img src="https://i.imgur.com/tFwocBQ.png" height="80%" width="80%" alt="osTicket Installation Wizard"/>
  
      -<p> Next, click "Add" to set new permissions. </p>
  
  <img src="https://i.imgur.com/LuVwQOG.png" height="80%" width="80%" alt="osTicket Installation Wizard"/>

  <img src="https://i.imgur.com/weJsqL3.png" height="80%" width="80%" alt="osTicket Final Setup"/>

  <img src="https://i.imgur.com/TZOCf8P.png" height="80%" width="80%" alt="osTicket Final Setup"/>

  <img src="https://i.imgur.com/IUz98C1.png" height="80%" width="80%" alt="osTicket Final Setup"/>

</p>
<p>15) Now, continue setting up osTicket in the browser. Click "Continue" on the osTicket page and fill in the required details, except for the Database Settings—we’ll do that next.</p>
<p align="center">
  <img src="https://i.imgur.com/ibsANG6.png" height="80%" width="80%" alt="osTicket Final Setup"/>
</p>

  
<p>16) We will want to download and install HeidiSQL from the Installation Files.</p>
<p align="center">
  <img src="https://i.imgur.com/y7uPAZY.png" height="80%" width="80%" alt="osTicket Final Setup"/>
      -<p> When the program is open we will create a new session in it. </p>

  <img src="https://i.imgur.com/5TVbERn.png" height="80%" width="80%" alt="osTicket Final Setup"/>

      -<p> Next, connect to the session and create a database named "osTicket."</p>

  <img src="https://i.imgur.com/fVaUCbC.png" height="80%" width="80%" alt="osTicket Final Setup"/>
</p>


<p>17) In HeidiSQL, right-click "Unnamed" on the left side, select "Create new," then "Database." Name the new database "osTicket." After that, go back to the osTicket browser and enter "osTicket" under MySQL Database.</p>
<p align="center">
  <img src="https://i.imgur.com/8AX2YKr.png" height="80%" width="80%" alt="osTicket Final Setup"/>

    -<p> The last step is cleanup. Delete the "setup" folder at C:\inetpub\wwwroot\osTicket\setup—only delete that folder, nothing else. Then, set the permissions for the ost-config.php file back to "Read" only.</p>
      <img src="https://i.imgur.com/ihKlcyj.png" height="80%" width="80%" alt="osTicket Final Setup"/>

  -<p> After creating the database, go back to the osTicket browser, complete the rest of the forms, and review everything. Once you're sure it's correct, click "Install Now!" If everything is set up, the image below will appear, and you can move on to the next step.</p>
  <img src="https://i.imgur.com/sOIdVbk.png" height="80%" width="80%" alt="osTicket Final Setup"/>

  -<p> Congrats! You've successfully installed and set up osTicket!</p>

  <img src="https://i.imgur.com/U5wyucx.png" height="80%" width="80%" alt="osTicket Final Setup"/>


</p>
