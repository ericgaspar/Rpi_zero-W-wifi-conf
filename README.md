# Raspberry Pi Zero W Headless Wifi setup

### Setup your WIFI Credentials
Insert your SD card with Raspbian into it into your computer and open the SD card - the drive will be labeled **boot**.

Copy `wpa_supplicant.conf` with the following code

```
country=FR
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1
network={
    ssid="MyWiFiNetworkssid"
    psk="MyWiFiPassword"
    key_mgmt=WPA-PSK
    }  
```

### Enable SSH

Create an empty file in the boot directory called **ssh** in the **boot** drive
