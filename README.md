# Smb-project-
This Project is about file sharing with permissions from linux to linux or windows smb(server message block) that uses the same FTP like windows

Welcome Dr Omyma Younis

this is a shared file from linux to windows 10 using smb tool (samba)

For P2P conn assignment

Created by: Ahmed Hany Fathy 19106371
____________________________________________________________________________________________________________________________________________________

First : Connect 2 computers or more on the same network & keep on mind the IP address of each one
**on my Galaxy s20 hotspot
>ahmed pc is 192.168.128.63
**on arabia home netwrok
>IP is 192.168.1.9

******Steps on linux to start samba

1. su -  \\change to super previeldge user (root)

2. cd /etc/samba   \\change direction to /etc/samba

3. systemctl start smb.service \\To start samba serv (to stop replace start with stop)
                                \\To view the status of smb service running or not(replace start with status)
                                **\\Preferable to restart the service if the IP changed ( systemctl restart smb.service)

4. nano smb.conf (to view configuration file using nano text editor (aslo can use vi or any editor)

_________________________________________________________________
**To access the service as a samba client from (Linux)
1. Dnf install samba (Be sure that smbclient service is installed)
2. systemctl start smb.service
3. write the following command with root 
   smbclient -W WORKGROUP -U ahmed //192.168.1.9/LinuxShare (replace the ip address with given ip depending on the connected network)
_____________________________________________________________________________________________________________________
******Steps on windows 10

1. open file manager 
2. Click on Network
3. type in search bar or replace network word or on browser  \\\192.168.128.63\LinuxShare  (LinuxShare is the name of the file path on linux Path: /home/ahmed/share)
4. type user: ahmed 
        Passwd: 123
5.Now you Can access the Shared Files from Linux to Windows :D        
