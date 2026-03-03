# Domain Integration & RSAT Administration

Domain Integration - Process of "connecting" a device or service to a central domain.

Remote Server Administration Tools(RSAT) Administration - Collection of Microsoft utilities that lets IT administrators manage Windows Server roles (like Active Directory, DNS, and DHCP) directly from their local Windows 10 or 11 workstation.

## Windows Installation

1. Navigate to Window 10 website and download Windows ISO
![Windows Installation](./screenshots/windows-installation.png)

2. Once downloaded, select Windows ISO and do the following:
- Select "Create installation media for another PC"
![Windows Installation](./screenshots/windows-installation-2.png)
- Select "ISO file" and save Windows ISO file in file explorer
![Windows Installation](./screenshots/windows-installation-3.png)
- Finish Setup

## Virtual Machine Setup for Windows 10(Helpdesk)

1. Open VirtualBox
- Create new Virtual Machine
- Setup VM Operating System, password and specify virtual hardware and diskware
![Windows Setup](./screenshots/windows-setup.png)

- Power on VM
- Add downloaded Windows ISO image To Boot up Windows
![Windows Setup](./screenshots/windows-setup-2.png)

## Windows Desktop Experience Setup

1. In Windows Setup,
- Select with Windows 10 Pro

![Windows Setup](./screenshots/windows-setup-3.png)

- Select "Custom Install Windows only"

![Windows Setup](./screenshots/windows-setup-4.png)

- Proceed With Default Setup

2. In Basic Setup,
- Select "Setup for personal use"
![Windows Basic Setup](./screenshots/basic-setup.png)

- Select "Offline account"
![Windows Basic Setup](./screenshots/basic-setup-2.png)

- Select "Limited Experience"
![Windows Basic Setup](./screenshots/basic-setup-3.png)

- Create User with no password
![Windows Basic Setup](./screenshots/basic-setup-4.png)

- Proceed with default setup

## Administrator Setup in Windows 10 VM
1. To enable an admin account, navigate to file explorer -> right-click "This PC" -> "Manage" -> System Tools -> "Local User and Groups" -> Users -> right-click on Administrator -> "Properties"
![Windows Basic Setup](./screenshots/basic-setup-5.png)

2. In Administrator Properties, select "Password never expires" and click "OK"
![Windows Basic Setup](./screenshots/basic-setup-6.png)

3. Right-click Administrator -> "set Password" -> create password
![Windows Basic Setup](./screenshots/basic-setup-7.png)

4. Sign out of user account(local) and Log in as Administrator account

5. In the Admin account to remove local account, navigate to file explorer -> right-click "This PC" -> "Manage" -> System Tools -> "Local User and Groups" -> Users -> right-click on Local Account (User) -> "Delete"
![Windows Basic Setup](./screenshots/basic-setup-8.png)

## Windows RSAT Installation (Server Manager) and Renaming Computer(Desktop 1)
Note: As a helpdesk/IT support, RSAT tools like server manager may not be given due to advanced access

1. Navigate to "System" -> Optional features(On Left Panel) -> select "Add a feature"
![RSAT Installation](./screenshots/rsat-installation.png)

2. Select the following RSAT Tools: 
- Active Directory Certificate Services Tools
- Active Directory Domain Services and Lightweight Directory Services Tools
- DHCP Server Tools
- DNS Server Tools
- Group Policy Management Tools
- Remote Desktop Services Tools
- Server Manager
![RSAT Installation](./screenshots/rsat-installation-2.png)

3. To rename Windows Computer, navigate to file explorer -> right-click "This PC" -> Properties -> "Rename This PC"
![RSAT Installation](./screenshots/rsat-installation-3.png)

## Installing TeamViewer to Windows VM

1. In Windows VM,
- Navigate to TeamViewer download website and download TeamViewer for Windows
- Install default setup for TeamViewer
![TeamViewer Installation](./screenshots/teamviewer-install.png)

## Add Computer to Domain (Connect Desktop 1 to Windows 10 Server)

1. To create a static IP address in order to connect to this machine to the domain, 
- navigate to Control Panel -> select "Network and Internet: View network status and tasks" -> "change adapter settings" -> "Ethernet" -> "Properties" -> select "TCP/IPV4"

2. In TCP/IPV4 properties,
- select "use the following IP address"
- Fill in the following IP address and DNS server address credentials
![Domain Integration](./screenshots/domain-integration.png)

3. Navigate to Devices (Top Panel) -> Network -> Network Settings -> Change Network Adapter to "Host-only Adapter" (This should be done for both Windows 10 VM and Windows Server VM)
![Domain Integration](./screenshots/domain-integration-2.png)

4. Navigate to File explorer -> right-click "This PC" -> Properties -> "Rename This PC (advanced)" -> select "Change" -> Select "domain", add domain name and enter admin credentials
![Domain Integration](./screenshots/domain-integration-3.png)

5. To Confirm domain integration is successful, try logging in with a User accounted created in the Windows Server Domain (Ex: helpdesk)
![Domain Integration](./screenshots/domain-integration-4.png)