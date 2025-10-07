
# Features 
- Breed Bootloader ✔
- Custom Mac addresses ✔
- LAN switch to WAN ✔
- WAN switch to LAN ✔
- ISP Mode
     - 4 WAN ISP = 1-WISP 3-WAN Ethernet ✔
- LAN Mode
     - 3 LAN Ethernet ✔
- WAN/VLAN | Guest LAN/VLAN ✔
- TTL mangling ✔
- Mult-ISP Load Balancing Seamless Failover ✔
- Multi-ISP Redundancy/Failover ✔
- Special connection ✔
- Priority ✔
- Isolation ✔
- DHCP relay ✔
- USB MOD
     - Ethernet to USB Adapter ✔
     - USB 4G/LTE Modem ✔
- Firewall ✔
- Speed limiter ✔
- VPN ✔
- MESH ✔
- Model number KN-2212 ✔
- CPU MT7628N 575 MHz ✔
- RAM 128 MB DDR2 ✔
- Flash memory, Dual Image 32 MB ✔
- Wi-Fi class N300 ✔
- Wi-Fi antennas 2.4 GHz: 2 external ✔
- Wi-Fi client capacity 2.4 GHz: Up to 75 ✔
- Ethernet ports 4 × 100 Mbps ✔
- WPS/Wi-Fi button	✔
- Mobile data connection ✔
- Mesh Wi-Fi System ✔
- 2.4 GHz Wi-Fi network	300 Mbps (802.11n) ✔
- 2T × 2R: 2SS, 40 MHz ✔
- IPoE/PPPoE routing	Up to 95 Mbps ✔
- L2TP/PPTP routing	Up to 95 Mbps ✔
- WireGuard throughput	Up to 45 Mbps ✔
- Mobile data network
- Supports 4G USB modem	✔
- Supports 3G USB modem	✔
- Maximum network speed	Up to 150 Mbps ✔
- Seamless roaming 802.11k/r/v	✔
- Pre-configured Wi-Fi protection	✔
- WEP, WPA-PSK	✔
- WPA2-PSK, WPA2-Enterprise	✔
- WPA3-PSK, WPA3-Enterprise, OWE	✔
- Multiple Wi-Fi networks Up to 7 SSID ✔
- Access control by MAC address	✔
- Wi-Fi Multimedia (WMM)	✔
- IPoE, PPPoE, PPTP, L2TP, 802.1x	✔
- Multi-WAN	✔
- Policy routing	✔
- Internet connection backup	✔
- Ping Check connectivity monitor	✔
- PPPoE/PPTP/L2TP pass-through	✔
- VLAN IEEE 802.1Q	✔
- Routing table (DHCP/Manual)	✔
- IntelliQoS 	✔
- DHCP (client/server)	✔
- IPv6 Dual Stack	✔
- NAT 	✔
- IGMP	✔
- UDP to HTTP proxy 	✔
- UPnP	✔
- Manual port forwarding	✔
- SPI firewall with protection against DoS attacks	✔
- PPTP (client/server)	✔
- L2TP over IPSec client/server	✔
- OpenVPN client/server	✔
- SSTP client/server	✔
- Ethernet-over-IP, IP-IP, GRE	✔
- IPsec VPN (client/server)	✔
- WireGuard	✔
- Dynamic DNS client 	✔
- Direct or cloud access via KeenDNS	✔
- HTTPS security for access via KeenDNS	✔
- Cloudflare DNS	✔
- SafeDNS parental control 	✔
- AdGuard ad blocker 	✔
- Traffic statistics per client	✔
- Bandwidth limit per client	✔
- Access schedule per client or interface	✔
- Guest hotspot with authentication (Captive Portal)	✔
- Troubleshooting and management
- Cloud-based Remote Network Monitoring and Management 	✔
- Mobile app for Android and iOS 	✔
- Web Interface with the Initial Setup Wizard and HTTPS security	✔
- Command Line (CLI) via TELNET/SSH	✔
- An option to control from external network	✔
- Backup and restore configuration	✔
- Automatic OS updates	✔
- System event logging	✔

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

