# Installing PDQ Deploy / Deploying PDQ / Software Packages


## PDQ
PDQ - stands for "Pretty Darn Quick", is a pair of Windows systems management tools, PDQ Deploy and PDQ Inventory used by IT professionals to manage and maintain multiple computers remotely.

PDQ Deploy - software deployment tool used by IT administrators to remotely install, update, or uninstall software on multiple computers at once — without having to manually visit each one.

Software Packages - Bundle of files and instructions needed to install a program automatically.

### Installing PDQ Deploy on Windows Server 

1. On Windows Server VM, 
- Navigate to "Devices" tab(on top panel) -> Insert Guest Additions CD image...
![PDQ Installation](./screenshots/pdq-install.png)

2. Navigate to file explorer -> This PC -> select "CD Drive Virtualbox Guest Additions"
![PDQ Installation](./screenshots/pdq-install-2.png)

2. On VirtualBox Guest Setup, select default setup options, install, and reboot system
![PDQ Installation](./screenshots/pdq-install-3.png)

3. This application allows us to share documents off of the Virtual Machine(from our host copmuter), since our VM's are not using Wifi, therefore cannot install applications on there own

4. To Create a Shared folder with our host computer,
- Navigate to "Shared Folder Settings"(on bottom right panel of VM)
![PDQ Installation](./screenshots/pdq-install-4.png) 

- In Shared Folder Settings, add a Share Folder -> Create a new folder(Ex: helpdesk lab ) -> select "Auto mount" -> click "OK"
![PDQ Installation](./screenshots/pdq-install-5.png)

- On File explorer, you should see the new shared folder under "Network Locations"
![PDQ Installation](./screenshots/pdq-install-6.png)

5. On your Host Computer,
- Navigate to a web browser, sign up and install PDQ deploy on PDQ installation page. Also place downloaded file in the shared folder (Ex: helpdesk lab)
![PDQ Installation](./screenshots/pdq-install-7.png)
![PDQ Installation](./screenshots/pdq-install-8.png)

6. To temporarily put Server on the network and install PDQ deploy, On Windows Server:
- refresh file explorer and place it on the desktop
![PDQ Installation](./screenshots/pdq-install-9.png)

- Navigate to "Devices" tab(on top panel) -> Network -> set Network to "Bridged Adapter" 
![PDQ Installation](./screenshots/pdq-install-10.png)

- Navigate to Control Panel -> "View network status and tasks" -> "Change adapter settings" -> right-click Ethernet -> Properties -> Internet Protocol Version 4(TCP/IPv4)
![PDQ Installation](./screenshots/pdq-install-11.png)

- On TCP/IPv4 Properties, select "Obtain an IP address automatically" and "Obtain DNS server address automatically" (Tip: save static IP address credentials for later)
![PDQ Installation](./screenshots/pdq-install-12.png)

- To confirm the server has network run on CMD, "ping 8.8.8.8", and you should get replies from the network
![PDQ Installation](./screenshots/pdq-install-13.png)

### Deploying PDQ on Windows Server (Installing PDFsam Basic application To the Windows Server using PDQ deploy)

1. Select PDQ Deploy file on your desktop and install Microsoft .NET framework 
![PDQ Deploy](./screenshots/pdq-deploy.png)

2. PDQ Deploy Setup, install default setup and launch PDQ Deploy (the new one, the old on can be recycled or deleted)
![PDQ Deploy](./screenshots/pdq-deploy-2.png)

3. To install PDFsam Basic, navigate to Package Library and download PDFsam Basic
![PDQ Deploy](./screenshots/pdq-deploy-3.png) 

4. To Deploy PDFsam Basic to a machine:
- Navigate to "Packages" folder" -> right-click "PDFsam Basic" -> Deploy Once -> select "Choose Target" -> Active Directory -> Computers
![PDQ Deploy](./screenshots/pdq-deploy-4.png)

- In "Select AD Target", move SERVER2016 to the Targets table click "OK", and select "Deploy now"
![PDQ Deploy](./screenshots/pdq-deploy-5.png)

- After the deployment, PDF Basic should appear on Server 2016's Desktop
![PDQ Deploy](./screenshots/pdq-deploy-6.png)

5. To take Windows Server back off the network: 
- Navigate to Control Panel -> "View network status and tasks" -> "Change adapter settings" -> right-click Ethernet -> Properties -> Internet Protocol Version 4(TCP/IPv4)

- On TCP/IPv4 Properties, fill original static IP address credentials
![PDQ Deploy](./screenshots/pdq-deploy-7.png)

- Navigate to "Devices" tab(on top panel) -> Network -> set Network to "Host-Only Adapter" 
![PDQ Deploy](./screenshots/pdq-deploy-8.png)

- To confirm everything is back its original settings, in CMD ping your domain and you should get replies
![PDQ Deploy](./screenshots/pdq-deploy-9.png)