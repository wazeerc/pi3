# Raspberry Pi Setup

## [DietPi](https://dietpi.com/docs/) (Headless)

1. Download the image from [here](https://dietpi.com/#download)
2. Flash the image on an SD Card using [balenaEtcher](https://etcher.balena.io/)
3. Set up Wi-Fi
   - Open the SD Card folder
   - Edit the `dietpi.txt` file and set `AUTO_SETUP_NET_WIFI_ENABLED` to `1`
   - Edit the `dietpi-wifi.txt` file and set the values of `aWIFI_SSID[0]` & `aWIFI_KEY[0]` to the desired WiFi network's SSID and Password
4. Boot the device and install the OS
5. Look for the device's IP address
    - `sudo nmap -sn 192.168.1.0/24`
    - or connect to a display via HDMI and run `hostname -I`
6. ssh onto the device
    - `ssh root@<PI's IP ADDRESS>`
7. Complete the OS installation process
8. Login using the default credentials; `login: root` & `password: dietpi`
9. Configure a Static IP Address in `dietpi-config > 7. Network Options: Adapters`
10. Run a backup using `dietpi-backup`
