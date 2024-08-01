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
- [Installation Files](https://github.com/rcruz04/osticket-prereqs/blob/main/install.files.md) (Insalled on VM or physical hardware)
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
<img width="1470" alt="Screenshot 2024-08-01 at 12 00 11 PM" src="https://github.com/user-attachments/assets/50abe40c-e5d1-4dc2-bd14-2ec2270bf92b">
</p>
<p>

Install the [PHP manager](https://drive.google.com/file/d/1Hdxax5lXfKAm2MwzCxI_JYyeOvPS6__V/view?usp=share_link). Click the link and go though the installation steps.
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 12 07 08 PM" src="https://github.com/user-attachments/assets/76a9f031-9c60-4142-840c-105aa49aae84">
</p>
<p>

Intsall the [Rewrite File](https://drive.google.com/file/d/1M5B3d9qcQLMTBCJPDsvy7qNCQwoy9uOk/view?usp=share_link) and run it.
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 12 09 36 PM" src="https://github.com/user-attachments/assets/312e4d14-7700-484f-835d-9bb1ea82bb63">
</p>
<p>
Go to the root of the opperating system and create the folder "PHP" so it should look like "C:\PHP"
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 12 16 15 PM" src="https://github.com/user-attachments/assets/9ddff2ac-6a51-4ad0-b01c-713b2368127f">
</p>
<p>

Download [PHP](https://drive.google.com/file/d/1Hdxax5lXfKAm2MwzCxI_JYyeOvPS6__V/view?usp=share_link) from the link and after its downloaded, extract the files into the PHP folder at the root of the OS.
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 12 20 52 PM" src="https://github.com/user-attachments/assets/35f1e042-4321-400a-a7b7-04a2f22ae572">
</p>
<p>

Install [VC](https://drive.google.com/file/d/1wwKD1XOiQ3CyB6RhuC7SOqTluTZbv7sl/view?usp=share_link) from the link.
</p>
<br />

<p> 
<h2>
  
  Download [MySQL](https://drive.google.com/file/d/1_WMQcnHuBCOs5GvaOTQPjrv70vxiuaNo/view?usp=share_link) and go though the installation steps. </h2>
<img width="1470" alt="Screenshot 2024-08-01 at 12 25 08 PM" src="https://github.com/user-attachments/assets/69edf1c1-f276-4f46-865c-9c1edf4896f1">
<h2>Typical Installation</h2>
<img width="1470" alt="Screenshot 2024-08-01 at 12 25 30 PM" src="https://github.com/user-attachments/assets/b184e872-739f-497c-be60-37dd7f49c715">
<h2>Standard Configuration</h2>
<img width="1470" alt="Screenshot 2024-08-01 at 12 27 12 PM" src="https://github.com/user-attachments/assets/136e034f-795e-4b37-86b9-0976a9b4b2e9">
<h2>This first option.</h2>
<img width="1470" alt="Screenshot 2024-08-01 at 12 27 51 PM" src="https://github.com/user-attachments/assets/295e3c8e-387c-45ad-b64b-90bd882407ed">
<h2>I used "Password1" here because its a lab but in real life youd want to use a secure password here.</h2>
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 12 41 21 PM" src="https://github.com/user-attachments/assets/3383122b-f968-4d35-8a18-523a567e565d">
</p>
<p>
Open IIS as an admin.
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 12 43 11 PM" src="https://github.com/user-attachments/assets/5a3804cf-ccbb-421b-9594-4098e3d7fcef">
</p>
<p>
Once opened, click where it says "PHP Manager" and then click "Register new PHP version" then go to the root of the OS then PHP then click on "php-cgi.exe"
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 12 46 43 PM" src="https://github.com/user-attachments/assets/da7f4fa5-7be2-49cc-8483-17d442b8e71c">
</p>
<p>
Back in the main menu, click restart to save the changes.
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 12 50 19 PM" src="https://github.com/user-attachments/assets/c811e3e8-4a43-4ca6-9bc2-65316a603c79">
</p>
<p>
  
Download [osTicket](https://drive.google.com/file/d/196gQKt8Y3ndznDgaeXUKqB41Hqk02QcM/view?usp=share_link) and transfer the "upload" folder to the "C:\inetpub\wwwroot" folder.
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 12 52 55 PM" src="https://github.com/user-attachments/assets/8854470e-f99d-4e0f-a0e9-76bc0dc60270">
</p>
<p>
Rename the upload folder to "osTicket".
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 12 46 43 PM" src="https://github.com/user-attachments/assets/7efef554-daa7-4f7d-ba67-5231902674d4">
</p>
<p>
Restart the server again.
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 12 55 17 PM" src="https://github.com/user-attachments/assets/c7a564c2-2ecf-4d2e-b877-31849933354b">
</p>
<p>
In the IIS go to sites, then defult website then osTicket. In that menu, click "Browse *.80" and  you should see a screen like this.
<img width="1470" alt="Screenshot 2024-08-01 at 12 58 42 PM" src="https://github.com/user-attachments/assets/046f5a43-9f03-4c15-abfc-4bffac2c2a79">
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 1 00 23 PM" src="https://github.com/user-attachments/assets/254851ea-5e5c-4c7b-9e5b-26ee29d0993d">
</p>
<p>
Back in the IIS, while in osTicket click the PHP manager, then go down to PHP extentions, then enable/disable extentions. In this menu find "php_imap.dll", "php_intl.dll", "php_opcache.dll" and enable them. Ive shown enabling "php_imap.dll" above.
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 1 04 55 PM" src="https://github.com/user-attachments/assets/fb01c933-e82e-4548-b26e-68f4e4c18906">
</p>
<p>
Refreshing the website should update the extentions that we enabled.
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 1 12 33 PM" src="https://github.com/user-attachments/assets/b9eec8fe-0cad-4750-b9b8-abbedd86e13b">
</p>
<p>
Go to "C:\inetpub\wwwroot\osTicket\include" and rename the "ost-sampleconfig.php" file to "ost-config.php"
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 1 14 55 PM" src="https://github.com/user-attachments/assets/3151a75e-7aae-4126-a04c-42eb185ee8a3">
</p>
<p>
Right-click "ost-config.php" file and then go to the security tab, then click advanced, then click "Disable inharitence".
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 1 17 18 PM" src="https://github.com/user-attachments/assets/9c15ce5b-ad03-46bc-8116-7fe062d58d3c">
</p>
<p>
Then click "Add", then "Select a principle", then type "everyone" and click "check names".
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 1 17 24 PM" src="https://github.com/user-attachments/assets/28082be9-1d70-4cdb-b617-e99f30344a08">
</p>
<p>
Then click "Full Control". It should look like the picture below.
<img width="1470" alt="Screenshot 2024-08-01 at 1 17 31 PM" src="https://github.com/user-attachments/assets/64942308-d98f-4524-85dc-08036c89d744">
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 1 27 13 PM" src="https://github.com/user-attachments/assets/76fcaa5d-fdb9-4507-8e88-bee4c437d5d6">
</p>
<p>
  
Download and install [HeidiSQL](https://www.heidisql.com/installers/HeidiSQL_12.3.0.6589_Setup.exe) and launch it when finished.
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 1 29 03 PM" src="https://github.com/user-attachments/assets/e24dd74e-39f9-4440-bc62-9ae4546bee4a">
</p>
<p>
Click new and type the password from earlier.
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 1 32 29 PM" src="https://github.com/user-attachments/assets/dbdc11a1-7d06-42f7-8e02-eb19c776e3ed">
</p>
<p>
Right-click and click "Create New" and then "Database" and name it "osTicket".
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 1 24 03 PM" src="https://github.com/user-attachments/assets/49261b6e-7ab6-4a08-a13e-7038803a639e">
</p>
<p>
Set up some basic credentals. You can put anything you want but this is what i put. MAKE SURE TO REMEMBER THE PASSWORD HERE.
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 1 35 57 PM" src="https://github.com/user-attachments/assets/38d42df8-fc80-43ff-8c2f-50abc8dce646">
</p>
<p>
Finish up the text boxes with the database name from Heidi, put root as the username and the passord as the one set up earlier when installing the SQL server.
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 1 44 24 PM" src="https://github.com/user-attachments/assets/203a61b0-6915-443a-9fb3-52f06994f888">
</p>
<p>
If everything went well you should get a screen that looks like this.
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 1 48 03 PM" src="https://github.com/user-attachments/assets/b733fc7f-82fc-4e8c-8026-7ba94811eb80">
</p>
<p>
Go to "C:\inetpub\wwwroot\osTicket\" and delete the "setup folder there."
</p>
<br />

<p>
<img width="1470" alt="Screenshot 2024-08-01 at 1 52 49 PM" src="https://github.com/user-attachments/assets/554e14ca-9611-4ce2-b1f4-ca8e4db6c627">
</p>
<p>
Go to "C:\inetpub\wwwroot\osTicket\include" and change the permisions of the "ost-config.php" file by unchecking the write tab.
</p>
<br />





