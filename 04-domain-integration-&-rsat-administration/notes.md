# Domain Integration & RSAT Administration

## Windows Installation

1. Navigate to Window 10 website and download Windows ISO
![Windows Installation](./screenshots/windows-installation.png)

2. In Windows 10 setup,
- Select "Create installation media for another PC"
- Select "ISO file" and save Windows ISO file in file explorer
- Finish Setup
![Windows Installation](./screenshots/windows-installation-2.png)
![Windows Installation](./screenshots/windows-installation-3.png)

## Windows Virtual Machine Setup

1. Open VirtualBox
- Create new Virtual Machine
- Setup VM Operating System, password and specify virtual hardware and diskware
![Windows Setup](./screenshots/windows-setup.png)

- Power on VM
- Add downloaded Windows ISO image To Boot up Windows
![Windows Setup](./screenshots/windows-setup-2.png)

### Windows Desktop Experience Setup

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

### Administrator Setup
1. To enable admin account, navigate to file explorer -> right-click "This PC" -> "Manage" -> "Local User and Groups" -> Users -> right-click on Administrator -> "Properties"
![Windows Basic Setup](./screenshots/basic-setup-5.png)

2. In Administrator Properties, select "Password never expires" and click "OK"
![Windows Basic Setup](./screenshots/basic-setup-6.png)

3. Right-click Administrator -> "set Password" -> create password
![Windows Basic Setup](./screenshots/basic-setup-7.png)

4. Sign out of user account(local) and Log in as Administrator account

5. To remove local account, navigate to file explorer -> right-click "This PC" -> "Manage" -> "Local User and Groups" -> Users -> right-click on Local Account (User) -> "Delete"
pic

## Windows RSAT Installation (Server Manager)
Note: As a helpdesk/IT support, RSAT tools like server manager may not be given due to advanced access

1. Navigate to "add or remove programs" -> "Optional features" -> "Add a feature"
pic

2. Select the following RSAT Tools: 
- Active Directory Certificate Services Tools
- Active Directory Domain Services and Lightweight Directory Services Tools
- DHCP Server Tools
- DNS Server Tools
- Group Policy Management Tools
- Remote Desktop Services Tools
- Server Manager
pic