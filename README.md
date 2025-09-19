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
pkg update && pkg upgrade -y && pkg install wget -y && wget -qO- https://raw.githubusercontent.com/xiv3r/termux-openwrt-invasion/refs/heads/main/openwrt-invasion.sh | sh && cd openwrt-invasion && ls
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

<img src="https://github.com/xiv3r/Xiaomi_4C_KeeneticOS/blob/main/openwrt_invasion.png">

# Telnet
```
telnet 192.168.31.1
```
login: root
password: root

# Flash Firmware 
> Download the firmware
```
wget -O /tmp/kn2212.bin https://github.com/xiv3r/Xiaomi_4C_KeeneticOS/releases/download/4.1.7/Full_Xiaomi_4C_KeeneticOS_4.1.7.bin
```
> Flash the firmware
```
mtd -r write /tmp/kn2212.bin ALL
```

<details><summary></summary>

# Mlti-isp load balancing with seamless failover config 
```
    set net.ipv4.ip_forward 1
    set net.ipv4.tcp_fastopen 3
    set net.ipv4.tcp_mtu_probing 1
    set net.ipv4.conf.all.rp_filter 0
    set net.core.default_qdisc fq_codel
    set net.ipv4.conf.all.secure_redirects 0
    set net.ipv4.conf.all.accept_redirects 0
```
</details>

