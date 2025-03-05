# HamClock

## 	HamClock is a kiosk-style application that provides real time space weather, radio propagation models, operating events and other information particularly useful to the radio amateur. HamClock was introduced in my October 2017 QST article and continues to be maintained and expanded.


HamClock Installation on Raspberry Pi Zero 2 W
- Prepare the Raspberry Pi OS
  -  Burn the SD card with Raspberry Pi OS using the Raspberry Pi Imager:
    - Device: Select Raspberry Pi Zero 2 W.
    - OS: Choose Raspberry Pi OS (64-bit).
    - Storage: Select the SD card and click Next
    - Customization:
      - General Tab:
        - Set hostname (e.g., hamclock).
        - Configure OS username and password.
        - Set WiFi SSID and password.
        - Set locale settings to US, Chicago.
    - Services Tab:
        - Enable SSH and use password authentication.
    - Options Tab: Leave as default.
Save and confirm Apply OS customizations.
Burn the image to the SD card.
2. Insert the SD card into the Raspberry Pi and boot it up.
3. Connect via SSH:
Use the hostname (hamclock.local) or the assigned IP address.
Example:
ssh username@hamclock.local

2. Update the System
Run the following commands:
sudo apt-get update
sudo apt-get upgrade -y

3. Install HamClock
Follow the official installation instructions from HamClock’s website.
1. Open a terminal on the Raspberry Pi desktop GUI:
Click on Raspberry → Accessories → Terminal.
2. Download and run the installer:
cd
curl -O https://www.clearskyinstitute.com/ham/HamClock/install-hc-rpi
chmod u+x install-hc-rpi
./install-hc-rpi
3. Answer installation prompts:
Web access only (no hardware display)? → y
Select HamClock size:
1) 800x480
2) 1600x960
3) 2400x1440
4) 3200x1920

Choose Option 3 (2400x1440).
Auto-start on reboot? → y
(This adds a crontab entry.)
Build process takes ~8 minutes.
4. Reboot the system:
sudo reboot now

4. Access HamClock
1. On another machine, open a web browser and go to:
http://[ip-address-or-hostname]:8081/live.html
Example:
http://hamclock:8081/live.html
2. The HamClock configuration page will open.
Enter Callsign and Location info.
Use LatLong.net to find coordinates (e.g., 40.477, -88.993).

🎉 That’s it! HamClock is now installed and accessible on your Raspberry Pi!

