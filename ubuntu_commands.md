Author: domi-lab

1. Mount and unmount one ubuntu PC other ubuntu PC: 

- Mount other ubuntu PC
    + Example: sudo sshfs -o allow_other odroid@192.168.0.104:/ /home/domi_lab/workspace/remote/odroid/
- Unmount other ubuntu PC: 
    + Example: sudo umount /home/domi_lab/workspace/remote/odroid
2. Use or pass sudo password in shell scrip: 
    + Use -S option and |
    + Example: echo "PASSWORD" | sudo -S apt-get update
    + Reference: https://twpower.github.io/164-how-to-use-sudo-password-in-shell-script-en

3. Remote Odroid from ubuntu/windown: 
    + Set auto login to Odroid : access to /usr/share/lightdm, open file 50-ubuntumate.conf as admin, add the following line: autologin-user=odroid
    + Open Odroid terminal
    + $ sudo apt update
    + $ sudo apt-get upgrade
    + $ sudo apt install x11vnc
    + Check Odroid IP address: ifconfig
    + On Odroid screen, click Menu, search and open Startup Application
    + Click Add button and add the following information into blanks. name: x11vnc, command: /usr/bin/x11vnc -bg -reopen -forever, comment: X11VNC Server, then save it. In this, -forever: keep running, -reopen: reopen when adding new client.
    + Restart Odroid
    + On ubuntu/linux, install vnc viewer
    + Type Odroid IP address on VNC Server: 192.168.0.100 (example)
    + Fill in Name of connection: Odroid N2 (any name)
    + Done
    + Reference: https://www.youtube.com/watch?v=VLNBEv_x3ng

4. Use crontab to schedule ubuntu PC
    + Reference: https://www.digitalocean.com/community/tutorials/how-to-use-cron-to-automate-tasks-ubuntu-1804