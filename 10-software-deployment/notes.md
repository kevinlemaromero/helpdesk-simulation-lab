# Installing PDQ / Deploying PDQ / Software Packages


## PDQ
PDQ - stands for "Pretty Darn Quick", is a pair of Windows systems management tools, PDQ Deploy and PDQ Inventory used by IT professionals to manage and maintain multiple computers remotely.

### Installing PDQ on Windows Server 

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
- Navigate to a web browser and install PDQ on PDQ installation page
pic

6. To temporarily put Server on the network, On Windows Server:
- refresh file explorer and place it on the desktop
pic

- Navigate to "Devices" tab(on top panel) -> Network -> set Network to "Bridged Adapter" 
pic

- Navigate to Control Panel -> "View network status and tasks" -> "Change adapter settings" -> right-click Ethernet -> Properties -> Internet Protocol Version 4(TCP/IPv4)
pic

- On TCP/IPv4 Properties, select "Obtain an IP address automatically" and "Obtain DNS server address automatically" 

7. 

### Deploying PDQ on Windows Server


## Software Packages
Software Deployment - installing, updating, or distributing software to multiple computers — usually across a network — in an automated and controlled way.

Software Packages - Bundle of files and instructions needed to install a program automatically.
