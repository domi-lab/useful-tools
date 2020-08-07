Author: domi-lab

- Mount other ubuntu PC:  
    + Example: sudo sshfs -o allow_other odroid@192.168.0.104:/ /home/domi_lab/workspace/remote/odroid/
- Unmount other ubuntu PC: 
    + Example: sudo umount /home/domi_lab/workspace/remote/odroid
- Use or pass sudo password in shell scrip: 
    + Use -S option and |
    + Example: echo "PASSWORD" | sudo -S apt-get update
    + Reference: https://twpower.github.io/164-how-to-use-sudo-password-in-shell-script-en
