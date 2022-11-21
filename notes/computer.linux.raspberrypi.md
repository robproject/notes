---
id: 8um63expliuf60a3ipojudy
title: Raspberrypi
desc: ''
updated: 1657236299596
created: 1642472020670
---
# Software
## Setup
### Headless
1. download lates .img
2. delete partitions on microsd
3. flash .img to microsd with rufus
3. add empty, extensionless file ssh
4. add wpa_supplicant.conf and update network:

	country=US
	ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
	update_config=1
	
	network={
	scan_ssid=1
	ssid="your_wifi_ssid"
	psk="your_wifi_password"
	}

5. In terminal, ssh pi@ipi.pip.ip.ip
6. login, password is 'raspberry'
7. sudo apt update & upgrade
8. sudo apt install xrdp - rdp won't be able to login with pi, another user must be created
9. add user USER for xrdp
10. login with windows rdp


# Hardware
## I/O
### Header
Double Column Left-Right Format
| Pin | Value  | Connected | Pin | Value  | Connected |
|-----|--------|-----------|-----|--------|-----------|
| 1   | 3V3    | -         | 2   | 5V     | -         |
| 3   | GPIO2  | -         | 4   | 5V     | -         |
| 5   | GPIO3  | -         | 6   | GND    | -         |
| 7   | GPIO4  | -         | 8   | GPIO14 | -         |
| 9   | GND    | -         | 10  | GPIO15 | -         |
| 11  | GPIO17 | -         | 12  | GPIO18 | -         |
| 13  | GPIO27 | -         | 14  | GND    | -         |
| 15  | GPIO22 | -         | 16  | GPIO23 | -         |
| 17  | 3V3    | -         | 18  | GPIO24 | -         |
| 19  | GPIO10 | -         | 20  | GND    | -         |
| 21  | GPIO9  | -         | 22  | GPIO25 | -         |
| 23  | GPIO11 | -         | 24  | GPIO8  | -         |
| 25  | GND    | -         | 26  | GPIO7  | -         |
| 27  | GPIO0  | -         | 28  | GPIO1  | -         |
| 29  | GPIO5  | -         | 30  | GND    | -         |
| 31  | GPIO6  | -         | 32  | GPIO12 | -         |
| 33  | GPIO19 | -         | 34  | GND    | -         |
| 35  | GPIO19 | -         | 36  | GPIO16 | -         |
| 37  | GPIO26 | -         | 38  | GPIO20 | -         |
| 39  | GND    | -         | 40  | GPIO21 | -         |
