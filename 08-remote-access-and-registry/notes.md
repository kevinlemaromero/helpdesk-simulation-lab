# Windows Remote/ Remote Registry / Remote Desktop

## Remote Desktop
Remote Desktop - Technology that allows a user to access and control a computer or server from a different physical location using a separate device, often called the "client," over a network connection (like a local network or the internet).

### Enable Remote Desktop on Desktop 2(User Account)

1. Navigate to File Explorer -> right-click "This PC" -> Properties -> select Advanced system settings and use admin credentials to allow changes/access(ex: "helpdesk" admin)
![Enable Remote Desktop](./screenshots/enable-remote-desktop.png)
![Enable Remote Desktop](./screenshots/enable-remote-desktop-2.png)

2. In System Properties -> "Remote" tab, 
- Select "Allow remote connections to this computer"
- In "Select Users", verify admin has access by adding to "Remote Desktop Users
![Enable Remote Desktop](./screenshots/enable-remote-desktop-3.png)
![Enable Remote Desktop](./screenshots/enable-remote-desktop-4.png)

3. To confirm Remote Desktop Remote is enabled,
- Log into Windows Client (Desktop 1) as helpdesk admin
- Navigate to "Remote Desktop Connection"
![Enable Remote Desktop](./screenshots/enable-remote-desktop-5.png)

- Connect to Desktop 2 (name: desktop2) with admin credentials for access

- Both Machines would have to verify to connection, and once verified the user account (Ex: danny) will be logged out and admin(ex:helpdesk) would have access to the users files and much more.
![Enable Remote Desktop](./screenshots/enable-remote-desktop-6.png)

### Advantages of Remote Desktop (Admin(Desktop 1) using Remote Desktop on User(Desktop 2))

1. To Access the Users Files while on Remote Desktop, navigate to File Explorer -> "This PC" -> Local Disk -> Users -> User Account (Ex: danny)
![Enable Remote Desktop](./screenshots/enable-remote-desktop-6.png)

2. Remote Desktop Advantages include,
- Remote Access to Work Systems
- Faster Troubleshooting and Support
- Secure Connections
- Increased Productivity
- Cost Savings

## Remote Registry 
Windows Registry - database that stores all the important settings and configurations for your computer’s operating system, hardware, software, and user accounts.

Remote Registry - Lets IT admins view or edit another computer’s registry remotely, mainly for management or troubleshooting

### Determining Share Drives with Remote Registry

1. To enable Remote Registry, in User account (Desktop 2),
- Navigate to "Services"(run as adminisitrator and use admin credentials to access) -> Remote Registry
- In Remote Registry Properties, make "Startup type: Automatic", "apply" and select "start"
![Remote Registry](./screenshots/remote-registry.png)

2. To use Remote Registry, in Admin account (desktop 1),
- Navigate to Registry Editor -> File -> "Connect Network Registry"
- In "Select Computer", add desktop to Remote to(Ex: desktop2)
![Remote Registry](./screenshots/remote-registry-2.png)

3. Using Remote Registry, the Admin can access the user's(desktop2) shared drives and much more.
![Remote Registry](./screenshots/remote-registry-3.png)

## Windows Remote
Windows Remote - set of tools thats allows you to connect to a remote computer (like a work PC or server) and use it as if you were sitting right in front of it.

C$ - hidden administrative share that allows admins to remotely access a computer’s C: drive for management and support tasks.

### How to setup Windows Remote with a User

1. To enable Windows Remote , in User account (desktop 2)
- Navigate to Control Panel -> System and Security -> "Launch Remote Assistance" -> "Invite someone to trust to help you" -> "Save this invitation as a file" (recommend: save file on desktop)
![Windows Remote](./screenshots/windows-remote.png)

2. To use Windows Remote, in Admin account (desktop 1),
- Navigate to Control Panel -> System and Security -> "Launch Remote Assistance" -> "Help someone who has invited you" -> "Use an invitation file"
![Windows Remote](./screenshots/windows-remote-2.png)

- In File Explorer, search for path of user desktop (Ex: \\desktop2\c$) -> Users -> select user account(Ex: danny) -> Desktop(or where invitation file was placed) -> open file
![Windows Remote](./screenshots/windows-remote-3.png)

- Enter invitation password given to user
![Windows Remote](./screenshots/windows-remote-4.png)

- Notify User to allow you to connect to their computer

3. In Windows Remote you can,
- Guide User by using the left panel to ask/answer any questions or concerns
- Request control of user's desktop in order to access their system to better assist them
![Windows Remote](./screenshots/windows-remote-5.png)
![Windows Remote](./screenshots/windows-remote-6.png)
