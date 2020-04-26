#!/bin/bash
# Step 1: update the server with latest package
apt-get update

# Step 2: install the standard XRDP package from the Ubuntu repository
apt-get -y install xrdp

# Step 3: install the alternate desktop environment e.g. xfce4
apt-get -y install xfce4

# Step 4: configure the ubuntu server for xrdp to know that the xfce destop environment will be used intead of Gnome or Unity.
echo "xfce4-session">~/.xsession

# Step 5: start the xrdp service on ubuntu server
/etc/init.d/xrdp start

# Step 6: check status of xrdp service
/ect/init.d/xrdp status

# Step 7: test the xrdp connection on the ubuntu server through a RDP client on a window machine "Remode desktop connection".start the Remode Desktop Connection on window system and then type the IP address of the ubuntu server. you will see xrdp login screen of ubuntu enter username and password of the server and prress OK.you will see a dialog box showing the login initialization process.It will lead to the xfce desktop
# option 1 : type window R and then mstsc
# option 2 : Window Key+Q and find Remote Desktop COnnection
# Option 3 : Window Key + F and find Window desktop Connection
# Option 4 : Window key + R and type control panel and search Remote App and Desktop Connection ->Access RemoteApp and Desktops

# Ref : https://www.isunshare.com/windows-8/where-is-remote-desktop-connection-in-windows-8.html
