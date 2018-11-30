+ Download RaspberryPi DietPi Image from [dietpi.com](https://dietpi.com).
+ Open `/boot` partition on sdcard, and locate the file called dietpi.txt and open it with editor.
  + Set `AUTO_SETUP_NET_WIFI_ENABLED=1` .
+ Locate the file called dietpi-wifi.txt and open it with editor.
  + Change `aWIFI_SSID[0]="MySSID"` and `aWIFI_KEY[0]="MyWifiKey"` .
+ Locate the file called cmdline.txt and open it with editor.
  + Change `console=serial0,115200` to `console=AMA0,115200`.
  + append `modules-load=dwc2,g_ether` at the end of the file.
+ Locate the file called config.txt and open it with editor.
  + Add option `dtoverlay=dwc2` below `#-------SoundCard-------` section. //@pfoof why is that ? why in Sound Card ?
+ Save chanages and run your Raspberry Pi.
+ Login onto root with login: `root` password: `dietpi` .
+ In dietpi-config step, change `ssh-server` from `bearssh` to `openssl` and proceed with minimal image **Go >> Start install**. This will complete the 1st run setup of DietPi. Additional software will be installed in next steps.
+ Login onto `dietpi` user and:
  + Update packages `sudo apt update` .
  + Install openjdk8 runtime `sudo apt install openjdk-8-jre` .
  + *(Optional)* Install mDNS `sudo apt install avahi-daemon` so you can resolve your device with `dietpi.local` .
  + Install DHCP Server with `sudo install isc-dhcp-server`
  + Replace `/etc/dhcp/dhclient.conf` with `https://github.com/RaspberryWallet/RaspberryWallet/blob/master/etc/dhcp/dhclient.conf`
  + Replace `/etc/dhcp/dhcpd.conf` with `https://github.com/RaspberryWallet/RaspberryWallet/blob/master/etc/dhcp/dhcpd.conf` 
  + Replace `/etc/network/interfaces`with `https://github.com/RaspberryWallet/RaspberryWallet/blob/master/etc/network/interfaces`
  + Replace `/etc/hostname` with `https://github.com/RaspberryWallet/RaspberryWallet/blob/master/etc/hostname`
  + Replace `/etc/hosts` with `https://github.com/RaspberryWallet/RaspberryWallet/blob/master/etc/hosts`
  
  
