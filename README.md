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

- Windows 10 </b> 

<h2>List of Prerequisites</h2>

- Microsoft Azure Subscription / Hardware to install on.
- [Installation Files](https://drive.google.com/drive/folders/1PZniuytu3z9D4xLDlzRqx_tZpf9Lw2zZ?usp=share_link) (Insalled on VM or physical hardware)
  - [PHPManager](https://drive.google.com/file/d/1nX1po3OYIT0eAKMuQWlHj4EzpsMIsdV7/view?usp=share_link)
  - [Rewrite File](https://drive.google.com/file/d/1M5B3d9qcQLMTBCJPDsvy7qNCQwoy9uOk/view?usp=share_link)
  - [PHP 7.3.8](https://drive.google.com/file/d/1Hdxax5lXfKAm2MwzCxI_JYyeOvPS6__V/view?usp=share_link)
  - [VC_redist.x86](https://drive.google.com/file/d/1wwKD1XOiQ3CyB6RhuC7SOqTluTZbv7sl/view?usp=share_link)
  - [MySQL 5.5.62](https://drive.google.com/file/d/1_WMQcnHuBCOs5GvaOTQPjrv70vxiuaNo/view?usp=share_link)
  - [osTicket](https://drive.google.com/file/d/196gQKt8Y3ndznDgaeXUKqB41Hqk02QcM/view?usp=share_link)
  - [HeidiSQL](https://www.heidisql.com/installers/HeidiSQL_12.3.0.6589_Setup.exe)

<h2>Installation Steps</h2>

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 11 20 04 AM" src="https://github.com/user-attachments/assets/0b926583-0a0c-4f98-ae94-add5a5a72a0a">
</p>
<p>
In the Azure portal, create a resource group and name it "osTicket". To make a resource group, go to the search bar and search "resource group" and click enter, then click on the cube with a brackets and you sould see the set-up screen.
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 11 21 47 AM" src="https://github.com/user-attachments/assets/848f34bb-0fde-43cb-b4ef-1b759ea6b970">
</p>
<p>
In the resource group, create a Windows 10 pro VM with the specs listed above. To make the VM, while in the resource group click "Create" and a menu should come up. In the marketplace search bar, search "Virtual Machine" and click on the monitor with the cube in it. Name the VM "osTicket" with the user "labuser" and whatever password you can remember and click create. This should start the deploymnt of the windows VM.
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 11 28 26 AM" src="https://github.com/user-attachments/assets/f13d0502-b74a-425a-845b-0fb9b73e3153">
</p>
<p>
Find the public IP of the new VM. In the overview of the VM you should find the public IP of the VM, youll need this later to remotely connect to it to use it later.
</p>
<br />

<p>
<img width="711" alt="Screenshot 2024-08-01 at 11 30 40 AM" src="https://github.com/user-attachments/assets/84dd210e-6c79-4a23-9745-4a2acfad4810">
</p>
<p>
Remote desktop into VM. Using "Microsoft Remote Desktop" on mac or simply remote login on windows, log into the VM using the public IP and username and password you set in the Azure portal.
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 11 41 33 AM" src="https://github.com/user-attachments/assets/214932eb-3f86-44c9-b669-937713b7ac7d">
</p>
<p>
In the control panel, click "Internet Information Services" and make sure the management console is selected.
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 11 46 15 AM" src="https://github.com/user-attachments/assets/a3446437-57fe-4957-a3e4-9d7fa93b6029">
</p>
<p>
In the same window, go to "World Wide Web Services" and under "Application Develoupment Features" select "CGI".
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 11 46 28 AM" src="https://github.com/user-attachments/assets/c809783a-25b2-46f9-ae52-ad0b9c10d61d">
</p>
<p>
Under "Application Develoupment Features" click on "Common HTTP Features" and select all the boxes. After selecting all the layed out boxes, hit ok and windows should install all the features.
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 11 37 54 AM" src="https://github.com/user-attachments/assets/8007beb2-168b-4cc6-89c6-8053145b30aa">
</p>
<p>
In the VM go to "https://github.com/rcruz04/osticket-prereqs/" to make installing the files a little easier.
</p>
<br />

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
