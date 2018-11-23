+ Download RaspberryPi DietPi Image from [dietpi.com](https://dietpi.com).
+ Open `/boot` partition on sdcard, and locate the file called dietpi.txt and open it with editor.
  + Set `AUTO_SETUP_NET_WIFI_ENABLED=1` .
+ Locate the file called dietpi-wifi.txt and open it with editor.
  + Change `aWIFI_SSID[0]="MySSID"` and `aWIFI_KEY[0]="MyWifiKey"` .
+ Save chanages and run your Raspberry Pi.
+ Login onto root with login: `root` password: `dietpi` .
+ In dietpi-config step, change `ssh-server` from `bearssh` to `openssl` and proceed with minimal image **Go >> Start install**. This will complete the 1st run setup of DietPi. Additional software will be installed in next steps.
+ Login onto `dietpi` user and:
  + Update packages `sudo apt update` .
  + Install openjdk8 runtime `sudo apt install openjdk-8-jre` .
  + *(Optional)* Install mDNS `sudo apt install avahi-daemon` so you can resolve your device with `dietpi.local` .
  
