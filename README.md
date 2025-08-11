# About
Install KeeneticOS on Xiaomi Router 4C

# Requirements 
- Termux

# Install
- Openwrt invasion
```
pkg update && pkg upgrade -y && pkg install -y git python

git clone https://github.com/acecilia/OpenWRTInvasion.git

cd OpenWRTInvasion

pip install -r requirements.txt
```

# Setup
- Reset and Configure the router using the password 12345678

# Execute 
```
python remote_command_execution_vulnerability.py
```
- enter the password and enter to use tge default settings
- wait until the installation is finished

# Telnet
```
telnet 192.168.31.1
```
login: root
pass: root

# Install breed
```
cd /tmp
wget -O breed.bin 
```
- Flush the breed bootloader
```
mtd -r write /tmp/breed.bin Bootloader
```
# Flush firmware
- Go to the 192.168.1.1 upgrade -> bootloader
- upload the firmware then the router will reboot and done.


