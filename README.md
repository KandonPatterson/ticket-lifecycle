# Ticket Lifecycle
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Ticket Lifecycle: Intake Through Resolution</h1>
This guide shows you how to install osTicket v1.15.8 along with its prerequisites for lab/testing purposes on Windows 10 (21H2).<br />


<h2>📁1. Prepare the Installation Files</h2>

- Download and extract osTicket-Installation-Files.zip
- Extract the file to your Desktop
- The folder should be named: C:\Users<YourUsername>\Desktop\osTicket-Installation-Files


<h2>🌐 2. Install IIS with CGI</h2>

* Open Control Panel → Programs → Turn Windows features on or off
* Enable the following:
  - Internet Information Services
  - World Wide Web Services
  - Application Development Features
  - [X] CGI
<img width="381" height="339" alt="image" src="https://github.com/user-attachments/assets/b30bee1a-0377-45a7-a255-225e7ee9116c" />


<h2>3. Install Requied Components</h2>

From the osTicket-Installation-Files folder:
*Install PHP Manager for IIS

File: PHPManagerForIIS_V1.5.0.msi
*Install URL Rewrite Module

File: rewrite_amd64_en-US.msi

<img width="636" height="355" alt="image" src="https://github.com/user-attachments/assets/a8ea0105-80f7-4e9c-9031-5428b6af8df5" />

* Create PHP Directory: C:\PHP

Unzip PHP 7.3.8 ~~ <img width="237" height="22" alt="image" src="https://github.com/user-attachments/assets/08302827-9ca3-4902-a587-9a33331ef039" />

- File: php-7.3.8-nts-Win32-VC15-x86.zip

* Extract into: C:\PHP

* Install 'Visual C++ Redistributable'

* File: VC_redist.x86.exe

* Use Typical Setup

* After installation, run the MySQL Configuration Wizard

*Choose: Standard Configuration
  -Set username: root
  -Set password: root


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
