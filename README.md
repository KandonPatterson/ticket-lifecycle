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

- Unzip PHP 7.3.8 ~~ <img width="237" height="22" alt="image" src="https://github.com/user-attachments/assets/08302827-9ca3-4902-a587-9a33331ef039" />

- File: php-7.3.8-nts-Win32-VC15-x86.zip

* Extract into: C:\PHP

* Install 'Visual C++ Redistributable'

* File: VC_redist.x86.exe

* Use Typical Setup

* After installation, run the MySQL Configuration Wizard

* Choose: Standard Configuration

    -Set username: root
    -Set password: root

⚙️ 4. Configure IIS and PHP

* Open IIS Manager as Administrator
* Register PHP with IIS:
  - Click your server name
  - Open PHP Manager
  - Click: Register new PHP version
  - Path: C:\PHP\php-cgi.exe

<img width="664" height="541" alt="image" src="https://github.com/user-attachments/assets/43b02927-3745-4b83-b364-30ec58e1f7e9" />

* Reload IIS
  - Click IIS Manager:
  - Right-click your server → click Stop
  - Then Start

 📦 5. Install osTicket v1.15.8
 * From osTicket-Installation-Files folder, unzip: osTicket-v1.15.8.zip
 * Copy the upload folder to: C:\inetpub\wwwroot\

   <img width="411" height="151" alt="image" src="https://github.com/user-attachments/assets/3dce5dca-5771-4e7e-b74f-38b863f71e6a" />
* Rename: C:\inetpub\wwwroot\upload → C:\inetpub\wwwroot\osTicket
* Reload IIS again
  - Click Start → Stop

🌍 6. Launch osTicket in Browser
* Click IIS Manager
* Expand Sites → Default Web Site → osTicket
* On the right, click: Browse *:80 (http)
  
<img width="855" height="411" alt="image" src="https://github.com/user-attachments/assets/151766cd-de56-46bb-877a-7b44810c1981" />

In the browser, you’ll see some missing PHP extensions*

🧠 7. Enable Missing PHP Extensions

* Click IIS Manager
* Go to: Sites → Default Web Site → osTicket
* Double-click PHP Manager
* Click: Enable or disable an extension
  <img width="378" height="157" alt="image" src="https://github.com/user-attachments/assets/d3c23c8e-6181-4234-9fa6-6c7ac376b491" />

* Enable the following:
  - php_imap.dll
  - php_intl.dll
  - php_opcache.dll
* Refresh the osTicket browser page to verify changes

🔒 9. Set Permissions on the Configuration File
* Right-click ost-config.php → Properties → Security
* Click Advanced
* Click Disable inheritance → Remove all entries
  <img width="705" height="478" alt="image" src="https://github.com/user-attachments/assets/3c383c42-578a-42a0-94d6-fef369e9792c" />

* Add new permission:
  - User: Everyone
  - Permission: Full Control

























