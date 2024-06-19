<h1> Active Directory Configuration</h1>
<h2>Description</h2>
This project involves setting up and configuring Active Directory (AD) on a Windows Server 2019 environment. The goal is to create a functional AD domain, manage users and organisational units, and configure group policies to ensure a secure and well-organised network infrastructure. This setup includes installing Windows Server 2019 on a virtual machine, configuring the server roles, and establishing network connections between the server and client machines.

<h2>Key Objectives</h2>
Download and Install Windows Server 2019: Obtain the Windows Server 2019 ISO and set it up on a virtual machine.
Configure Active Directory: Set up AD DS (Active Directory Domain Services) and create a new forest and domain.
Manage Users and Groups: Create organisational units, add users, and manage groups within the AD structure.
Configure Group Policies: Implement group policies to manage user and computer settings across the domain.
Establish Network Connectivity: Configure network settings to allow communication between the server and client machines.
Integrate Client Machines: Add Windows 10 client machines to the domain and manage them through AD.
<h2>Utilities Used</h2>
Utilities: VirtualBox, Windows Server 2019, Windows 10 ISO
<h2>Environments Used></h2>
Operating Systems: Windows Server 2019, Windows 10
Hardware: Virtual Machines
Tools: Windows Server Manager, Active Directory Users and Computers, Group Policy Management

<h2>Program Walk-through:</h2>

Step 1: Download Windows Server 2019 ISO
<img src="https://i.imgur.com/N4INUDj.png" alt="Windows Server 2019 Download">
Search for Windows Server 2019:

Action: Open your preferred search engine (e.g., Google) and type "Windows Server 2019 download".
Explanation: This search will help you find the official Microsoft link for downloading Windows Server 2019.
Find the Microsoft Evaluation Centre:
<img src="https://i.imgur.com/X8TSF7F.png">
Action: Scroll through the search results to find the Microsoft link titled "Windows Server 2019 | Microsoft Evaluation Centre".
Explanation: The Microsoft Evaluation Centre provides a free trial version of Windows Server 2019.
Download the ISO:

Action: Click on "ISO DOWNLOADS" on the Microsoft Evaluation Centre page. Choose the appropriate language (for this demonstration, select English).
Explanation: The ISO file is a disc image that contains all the files needed to install Windows Server 2019. The download can take between 10 to 30 minutes, depending on your internet speed.
Step 2: Set Up Windows Server 2019 on VirtualBox
<img src="https://i.imgur.com/zfH405i.png" alt="VirtualBox New VM Setup">
<img src="https://i.imgur.com/8O2nVVY.png"> 
Create a New Virtual Machine:

Action: Open VirtualBox and click on "New".
<img src="https://i.imgur.com/C5dBZBJ.png">
Explanation: This starts the process of creating a new virtual machine (VM), which will host your Windows Server 2019 installation.
Name Your Virtual Machine:

Action: Enter a name for your VM (e.g., "Windows Server 2019"). Click on the drop-down menu for the ISO image and select the Windows Server 2019 ISO you downloaded.
Explanation: Naming your VM helps you identify it easily among other VMs you might have.
<img src="https://i.imgur.com/WaScJxL.png">
Configure Memory and CPU:

Action: Allocate 6GB of RAM and 3 CPUs for the VM. Click "Next".
Explanation: Adequate memory and CPU allocation ensures the VM runs smoothly without lag or performance issues.
<img src="https://i.imgur.com/k3HMVc6.png">

Remember to create a memorable username and password; this will be for logging in before gaining access to the Windows Server 2019:
<img src="https://i.imgur.com/0HAHZbc.png">
Step 3: Configure Virtual Hard Disk
<img src="https://i.imgur.com/3YZjRrp.png" alt="Virtual Hard Disk Setup">
Create a Virtual Hard Disk:
Action: Choose a virtual hard disk size between 50GB and 100GB. Click "Next" and then "Finish".
Explanation: The virtual hard disk will store the operating system and other files. A size of 50GB or more is recommended to ensure there's enough space for the installation and future updates.
Step 4: Finalize VM Configuration
<img src="https://i.imgur.com/NqoJTWO.png" alt="VM Final Configuration">
Review and Finalize:
Action: Review your VM settings and click "Finish".
Explanation: Ensure all settings are correct before finalizing the setup. This includes checking the name, ISO image, memory, CPU, and hard disk settings.
Boot Up Windows Server 2019:
Action: Start your Windows Server 2019 virtual machine and allow it to boot up. This process may take up to 5 minutes.
Explanation: During this phase, the virtual machine loads the necessary files and prepares for the installation process.
Language and Region Selection:
<img src="https://i.imgur.com/ovcIDxX.png"> <img src="https://i.imgur.com/SjljPt1.png">
Action: A pop-up box will appear to select the language, time format, currency format, and keyboard or input method. Choose "United Kingdom" for all options, then click "Install now".
Explanation: Selecting the correct language and region ensures that Windows Server 2019 is installed with the appropriate settings for your location.
Windows Server 2019 Edition Selection:
<img src="https://i.imgur.com/PNWd9lF.png">
Action: Choose "Windows Server 2019 Standard Evaluation (Desktop Experience)" from the available options.
Explanation: This edition provides a full desktop experience along with evaluation features. Click "Next" to proceed.
Accept Licence Terms:
<img src="https://i.imgur.com/CVRdtkl.png">
Action: Read and accept the licence terms by checking the box, then click "Next".
Explanation: Accepting the licence terms is necessary to proceed with the installation of Windows Server 2019.
Custom Installation:
<img src="https://i.imgur.com/V3cfwMi.png">
Action: Select "Custom: Install Windows only (advanced)" as the installation type.
Explanation: This option allows you to customise the installation settings, including choosing the disk where Windows will be installed.
Disk Selection:
<img src="https://i.imgur.com/halAGfU.png">
Action: Choose the virtual hard disk that you set up earlier for Windows Server 2019 installation. Click "Next" to continue.
Explanation: Selecting the correct disk ensures that Windows is installed in the intended location.
Installation Process:
<img src="https://i.imgur.com/21ml6D1.png">
Action: Windows will begin the installation process, which involves copying files, preparing for installation, and configuring settings. This process may take between 20 minutes to 1 hour, depending on your system's performance.
Explanation: During this phase, Windows Server 2019 installs the necessary files and prepares the system for first-time use.
<img src="https://i.imgur.com/b0Daup6.png"> <img src="https://i.imgur.com/rQeJF6n.png">
Now that you've reached the Windows Server 2019 startup screen, proceed by pressing Ctrl + Alt + Delete on your keyboard to unlock the system. Remember the administrator password you created earlier. Start the Server Manager by clicking on "Manage" and then "Add Roles and Features".
<img src="https://i.imgur.com/H2zIgQt.png">
Adding Roles and Features
Open Add Roles and Features Wizard:
<img src="https://i.imgur.com/sEpDtia.png">
After launching Server Manager, click on "Manage" and then "Add Roles and Features".
The "Add Roles and Features Wizard" pop-up box will appear.
Before You Begin:
<img src="https://i.imgur.com/1lg4nx9.png">
Click "Next >" to proceed.
Installation Type:
<img src="https://i.imgur.com/PuaZLSO.png">
Select "Role-based or feature-based installation" and proceed to the next configuration.
Server Selection:
<img src="https://i.imgur.com/0plHaCR.png">
Choose "Select a server from the server pool" and then select your Windows Server computer name.
<img src="https://i.imgur.com/tH3Bxj8.png">
Click "Next" to continue.
Server Roles:
<img src="https://i.imgur.com/trZin20.png">
Tick the box for "Active Directory Domain Services" and proceed by clicking "Next".
Features:
<img src="https://i.imgur.com/KMVqFHE.png">
Leave the features at their default settings.
Click "Next" to proceed with the Active Directory Domain Services (AD DS) installation.
Confirmation:
<img src="https://i.imgur.com/MsF6P6z.png">
Review the selected options and proceed by clicking "Install".
A message will inform you that the installation could take up to 45 minutes.
Post-Deployment Configuration
Active Directory Domain Services Configuration Wizard:
<img src="https://i.imgur.com/IyMKs9W.png"> <img src="https://i.imgur.com/5XV900O.png">
Click on "Add a new forest" and type a root domain name.
Proceed by clicking "Next".
Domain Controller Options:
<img src="https://i.imgur.com/otCdDlQ.png">
Create a password and keep all other settings at their default values.
Click "Next", but skip DNS options such as "Create DNS delegation".
Additional Options:
<img src="https://i.imgur.com/6gaE1Z7.png">
Verify the NetBIOS name assigned to the domain.
Click "Next" to proceed.
Paths and Review Options:
Skip these options and proceed.
Prerequisites Check:
<img src="https://i.imgur.com/PJ40IOc.png">
Click on "Install". This process could also take up to 45 minutes depending on your network speed.
Once completed, your Windows Server computer will reset.
<img src="https://i.imgur.com/duTKRmA.png">
Logging Back In
Log back into your server using your domain name/administrator credentials.
<img src="https://i.imgur.com/ObSfm4T.png"> <img src="https://i.imgur.com/yvXcTK8.png">
Configuring Active Directory Users and Computers
Launch Server Manager, click on "Tools", and select "Active Directory Users and Computers".
<img src="https://i.imgur.com/NdupDE9.png">
View > Advanced Features:
<img src="https://i.imgur.com/enARiAb.png"> <img src="https://i.imgur.com/LkcD0Ng.png">
Enable "Advanced Features" to access additional options.
Creating Organizational Units (OUs):
<img src="https://i.imgur.com/SEDHRy2.png">
Right-click on your domain and choose "New > Organizational Unit".
Name it "Cyber Security" and select "Protect container from accidental deletion".
<img src="https://i.imgur.com/3yxcCJW.png">
Adding Users:
<img src="https://i.imgur.com/TabeDax.png">
Add users with appropriate first and last names.
<img src="https://i.imgur.com/vEjsHXm.png"> 
Consider using a user logon name that uniquely identifies them.
Create passwords for these users, considering various security options.
 <img src="https://i.imgur.com/6GGd4St.png"> 
<img src="https://i.imgur.com/os16C3r.png">
Creating Groups:
<img src="https://i.imgur.com/Zpx0fGV.png">
Right-click and select "New > Group". Name it "Cyber Security Soc Analyst".
<img src="https://i.imgur.com/tj2rgeT.png">
Assigning Users to Groups:
<img src="https://i.imgur.com/fUNwdr2.png">
Highlight the users you created, right-click, and select "Add to a group".
Type the group name and click "OK".
<img src="https://i.imgur.com/oAOen4E.png">
Exploring User Properties:
<img src="https://i.imgur.com/zeRzX7A.png">
Right-click on a user and select "Properties".
Explore the various tabs such as "General", "Address", "Account", "Profile", "Telephones", "Organization", "Sessions", and "Environment" to configure user settings.
<img src="https://i.imgur.com/CZYwstq.png">
General:
First Name: Refers to the user's first name.
Last Name: Refers to the user's last name.
Initials: Typically used for abbreviations of the user's name.
Display Name: The name displayed in the directory and other services.
Description: A brief description of the user, often used for identification.
Office: The physical location or office of the user.
Telephone Number: The user's contact number.
Email: The user's email address.
Web Page: If applicable, this is the user's personal or professional website.
<img src="https://i.imgur.com/I2rAIL1.png">
Address:
Street: The user's street address.
P.O. Box: If applicable, the user's postal box number.
City: The city where the user resides.
State/Province: The state or province where the user resides.
Zip/Postal Code: The postal code of the user's area.
Country/Region: The country or region where the user resides.
<img src="https://i.imgur.com/i00cMxx.png">
Account:
Logon Hours: Specifies the times during which the user is allowed to log in. This restricts login access outside of specified hours.
<img src="https://i.imgur.com/9rsBbvv.png">
Log on To: Allows the user to log in to specific computers within the domain. This can restrict access to only specified machines.
<img src="https://i.imgur.com/CEeyKGW.png">
Account Expires: Sets an expiration date for the user account. After this date, the account will be disabled.
<img src="https://i.imgur.com/xbA18Mn.png">
Account Options:
User Must Change Password at Next Logon: Forces the user to change their password the next time they log in.
User Cannot Change Password: Prevents the user from changing their password.
Password Never Expires: Ensures the user's password never expires.
Account is Disabled: Disables the user's account, preventing login.
<img src="https://i.imgur.com/LyI1oMM.png">
Profile:
Profile Path: Specifies the path to the user's profile.
Logon Script: Specifies a script to run when the user logs in.
Home Folder: Specifies the path to the user's home folder.
<img src="https://i.imgur.com/ThVWSVF.png">
Telephone:
Office: The user's office telephone number.
Home: The user's home telephone number.
Mobile: The user's mobile phone number.
Fax: The user's fax number.
<img src="https://i.imgur.com/lWdGe53.png">
Organization:
Job Title: The user's job title or position within the organization.
Department: The department the user belongs to.
Company: The company the user works for.
Manager: The user's manager or supervisor.
Direct Reports: Employees who report directly to the user.
<img src="https://i.imgur.com/LECgIFc.png">
Sessions:
End a Disconnected Session: Specifies what action to take when a session is disconnected.
Active Session Limit: Limits the duration of an active session.
Idle Session Limit: Limits the duration of an idle session.
Allow Reconnection: Determines if users can reconnect to disconnected sessions.
<img src="https://i.imgur.com/Fy6XgvU.png">
Environment:
Start the following program at logon: Specifies a program to start automatically when the user logs in.
End a disconnected session: Specifies what action to take when a session is disconnected.
<img src="https://i.imgur.com/L3DMgm9.png">
Remote Control:
Enable Remote Control: Allows administrators to remotely control the user's session.
Require User's Permission: Determines if the user must give permission for remote control.
Level of Control: Specifies the level of control the remote administrator has over the user's session.
Download Windows 10 ISO Image:
<img src="https://i.imgur.com/xyUAD1g.png"> 
Search for a Windows 10 ISO image on your preferred search engine.
Click on the appropriate link to download the installation media.
Accept the license terms and choose to create installation media (USB flash drive, DVD, or ISO file).
<img src="https://i.imgur.com/dhstUL9.png"> <img src="https://i.imgur.com/YQBsmCD.png"> 
Select the default settings unless you need to change the language.
<img src="https://i.imgur.com/cdmXxUt.png">
Choose the ISO file option and proceed with the download. 
<img src="https://i.imgur.com/GBKSoCq.png">
This process could take up to 30 minutes depending on your internet speed.
<img src="https://i.imgur.com/0piYUX7.png">
Create a New Virtual Machine (VM) for Windows 10:
<img src="https://i.imgur.com/00OMIx6.png">
In your VM software, such as VirtualBox, click on "New" to create a new VM.
<img src="https://i.imgur.com/3KSARRl.png">
Set up a name for the VM and proceed with the default settings.
Allocate recommended resources, such as 2GB of RAM and 1 CPU, to ensure smooth performance.
<img src="https://i.imgur.com/OrEqiYF.png">
Set up a virtual hard disk for the VM, preferably around 50GB in size.
Finish setting up and configuring the VM.
<img src="https://i.imgur.com/Ih8dgAU.png">
Configure Windows 10 VM Settings:
<img src="https://i.imgur.com/Jb8NRMD.png">
Go into the settings of the Windows 10 VM.
Scroll down to storage settings and click on the empty storage device.
<img src="https://i.imgur.com/PMGs2X6.png">
Choose the disk file option and select the Windows 10 ISO file you downloaded.
<img src="https://i.imgur.com/1rlze7o.png">
Start the Windows 10 VM and let it load until the Windows setup screen appears.
Install Windows 10:
<img src="https://i.imgur.com/uBFZaTA.png">
Proceed with the Windows setup process, clicking "Next" until prompted.
<img src="https://i.imgur.com/Bvw0My8.png">
If prompted for a product key, select the option "I don't have a product key" as this is a demo setup.
<img src="https://i.imgur.com/a6Jiyr7.png"> <img src="https://i.imgur.com/NQAi25f.png">
Choose Windows 10 Home edition and accept the license terms.
<img src="https://i.imgur.com/TTaqbLF.png">
Select the custom installation option and choose the virtual hard disk you set up earlier.
<img src="https://i.imgur.com/XmPlhqe.png">
Follow the installation process, including copying files, preparing for installation, installing features, updates, and completing the setup. This could take up to 1 hour.
<img src="https://i.imgur.com/VqoNxGs.png">
Network Setup:

After the Windows 10 installation is complete, go back to your VM settings.
<img src="https://i.imgur.com/slK08hm.png">
Scroll down to network settings and attach the VM to a bridge adapter to enable internet connection.
<img src="https://i.imgur.com/MvP6YMs.png">
Repeat the same process for the Windows Server 2019 VM to ensure both computers have connectivity.
<img src="https://i.imgur.com/HhdJzWx.png">
Region and Keyboard Layout:
<img src="https://i.imgur.com/qrP12Ph.png">
Select your region and the appropriate keyboard layout.
<img src="https://i.imgur.com/xE98GtO.png">
Skip the option for a second keyboard layout.
<img src="https://i.imgur.com/j3jTm3I.png">
Initial Setup:
<img src="https://i.imgur.com/4skGDiF.png">
Wait for the system to load, which may take a few minutes.
Choose "Set up for personal use" and click "Next".
<img src="https://i.imgur.com/mCHta9G.png">
Account Setup:
<Img src="https://i.imgur.com/I8fowjM.png">
Opt for an offline account and choose "Limited experience".
<img src="https://i.imgur.com/6BARW6O.png">
Set up a name for the PC and create a strong password.
<img src="https://i.imgur.com/zlLnMzH.png"> <img src="https://i.imgur.com/X5vPEUs.png">
Answer security questions and click "Next".
<img src="https://i.imgur.com/UVvhtiT.png"> <img src="https://i.imgur.com/1O23RB0.png">
Optional Settings:
<Img src="https://i.imgur.com/Mla6ajo.png">
Click "Not Now" for the option to continue where you left off by importing from another browser.
<img src="https://i.imgur.com/SEzVwiD.png">
Turn off "Find my device" as it's not needed for this demonstration.
<img src="https://i.imgur.com/UbdJ76l.png">
Choose the second option for sending diagnostic data to Microsoft.
<img src="https://i.imgur.com/68wmavJ.png">
Turn off options for improving inking and typing.
<img src="https://i.imgur.com/68wmavJ.png">
Customization:
<img src="https://i.imgur.com/iLBUV7Q.png">
Skip the customization page by clicking "Skip".
Finalization:
<img src="https://i.imgur.com/jNcQsfu.png">
Allow the system to set up everything you configured, which may take several minutes.
Obtaining IP Addresses:
<img src="https://i.imgur.com/ITIPSZE.png">
On both the Windows Server 2019 and Windows 10 machines, open Command Prompt (CMD) and type "ipconfig /all" to retrieve the IP addresses.
Note down the IPv4 address of each machine.
<img src="https://i.imgur.com/uT1TBjp.png">
<img src="https://i.imgur.com/aUPcwKb.png">
Below you can see in the screenshot it's not sending data to windows server 2019.
<img src="https://i.imgur.com/dcVfQl8.png">
Configuring Windows Defender Firewall:
<img src="https://i.imgur.com/qAyVSHr.png">
On Windows 10, open Windows Defender Firewall with Advanced Security.
Navigate to "Inbound Rules" and create a new rule.
Choose "Custom rule type" and under scope, select the IP address of the Windows 10 machine.
Name the rule and click "Finish" to allow data connection to the Windows Server 2019 machine.
Repeat the same process for outbound rules, ensuring that the Windows 10 machine can send data.
