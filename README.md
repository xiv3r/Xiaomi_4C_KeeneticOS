# About
KeeneticOS for Xiaomi Mi Router 4C

# Features 
- Breed Bootloader
- LAN switch to WAN 
- WAN switch to LAN
- ISP Mode
     - 4 WAN ISP = 1-WISP 3-WAN Ethernet
- LAN Mode
     - 3 LAN Ethernet
- WAN/VLAN | Guest LAN/VLAN
- TTL plugin
- Mult-ISP Load Balancing Seamless Failover
- Multi-ISP Redundancy/Failover
- Special connection
- Isolated connection
- DHCP relay
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
- Termux Openwrt Invasion
```
pkg update && pkg upgrade -y && pkg install -y git python python-pip

git clone https://github.com/acecilia/OpenWRTInvasion.git

cd OpenWRTInvasion

pip install -r requirements.txt
```

# Setup
- Reset first and Configure the router using the password 12345678
- Connect to the Xiaomi SSID and execute the script below 👇 

# Execute 
```
python remote_command_execution_vulnerability.py
```
- enter the password and enter for the default settings
- wait until the installation is finished

# Telnet
```
telnet 192.168.31.1
```
login: root
password: root

# Install Breed Bootloader 
```
wget -O /tmp/breed.bin https://github.com/xiv3r/Xiaomi_4C_KeeneticOS/raw/refs/heads/main/cnBreed.bin
```
- Flush the breed bootloader
```
mtd -r write /tmp/breed.bin Bootloader
```
# Flush firmware
- Download the firmware first 

https://github.com/xiv3r/Xiaomi_4C_KeeneticOS/releases/download/4.1.7/keenetic_firmware_kn2212_v4.1.7.bin

- Go to the [192.168.1.1](http://192.168.1.1) and click the step 1 followed by clicking the step 2 upload the firmware and click step 3 then the router will reboot to KeeneticOS firmware.
<img src="https://github.com/xiv3r/Xiaomi_4C_KeeneticOS/blob/main/breed-bootloader.jpg">


# KeeneticOS firmware 
<img src="https://github.com/xiv3r/Xiaomi_4C_KeeneticOS/blob/main/multiwan.png">


