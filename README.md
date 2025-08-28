# About
KeeneticOS for Xiaomi Mi Router 4C

# Features 
- Breed Bootloader
- LAN switch to WAN
- WAN switch to LAN
- WAN/VLAN | Guest LAN/VLAN
- TTL plugin
- Mult-ISP Load Balancing Seamless Failover PBR
- Multi-ISP Redundancy/Failover PBR
- USB MOD
     - Ethernet to USB Adapter
     - USB 4G/LTE Modem
- Firewall
- Speed limiter
- VPN
- MESH And so much more...

# Requirements 
- Termux

# Install
- Openwrt invasion
```
pkg update && pkg upgrade -y && pkg install -y git python python-pip

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
wget -O breed.bin https://github.com/xiv3r/Xiaomi_4C_KeeneticOS/raw/refs/heads/main/cnBreed.bin
```
- Flush the breed bootloader
```
mtd -r write /tmp/breed.bin Bootloader
```
# Flush firmware
- Download the firmware

https://github.com/xiv3r/Xiaomi_4C_KeeneticOS/releases/download/4.1.7/keenetic_firmware_kn2212_v4.1.7.bin

- Go to the [192.168.1.1](http://192.168.1.1) upgrade -> bootloader
- upload the firmware then the router will reboot and done.


