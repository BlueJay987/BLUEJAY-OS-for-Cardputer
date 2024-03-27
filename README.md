# BLUEJAY-OS
Firmware for offensive pranks for Cardputer

## Name and Background
BLUEJAY-OS is a fork of M5-Bruce I have created to learn some ESP development and to mess around with the code of my favorite program.
Many thanks to the original developers of Bruce and Nemo, your stuff is one of the few resources i can find on this machine and i thank you for that :D

## Features
* [TV B-Gone](http://www.righto.com/2010/11/improved-arduino-tv-b-gone.html) port (thanks to MrArm's [HAKRWATCH](https://github.com/MrARM/hakrwatch)) to shut off many infrared-controlled TVs, projectors and other devices
* [AppleJuice](https://github.com/ECTO-1A/AppleJuice) iOS Bluetooth device pairing spam
* Bluetooth device notification spamming for SwiftPair (Windows) and Android
* WiFi EVIL Portal - A captive portal that tries to social engineer email credentials - saves usernames and passwords to SD Card (if inserted into a supported reader)
* WiFi SSID Scanner - Display 2.4 GHz SSIDs nearby and get information about them
* EEPROM-backed Settings for rotation, brightness and, automatic dimming
* Battery level and credits in settings menu
* Changelog - shows changes between versions
* DPWO-ESP32 - TBH i have no idea what this is but i kept it in in case you do
* Raw Sniffer - Saves PCAP to SD
* BadUSB - Reads payload on SD card /badpayload.txt
* Keyboard - Use as a keyboard USB input

## User Interface
There are three main controls:
* Home - Stops the current process and returns you to the menu from almost anywhere in BRUCE
* Next - Moves the cursor to the next menu option. In function modes, this usually stops the process and returns you to the previous menu.
* Select - Activates the currently-selected menu option, and wakes up the dimmed screen in function modes  

* Cardputer
  * Home: Tap the Esc/~/` key or the Left-Arrow/, key
  * Next/Prev: Tap the Down-Arrow/. key and Up-Arrow/; keys to navigate
  * Select: Tap the OK/Enter key or Right-Arrow/? key  

## EVIL Portal
In EVIL Portal mode, BRUCE reads the keyboard input for the SSID and activates a open WiFi, with DNS, DHCP and Web servers activated. 
* EVIL Portal serves a fake login page that claims to provide internet access if you log in.
* This is a social engineering attack, and will log the username and passwords entered on the page. 
* You can view these credentials by connecting to the portal from your own device and browsing to http://172.0.0.1/creds
* If your device has an SD Card reader with a FAT filesystem formatted card inserted, the usernames and passwords will be logged to nemo-portal-creds.txt on the SD Card for you to peruse later. 
* SD Card support is only enabled by default on the M5Stack Cardputer platform. It can be enabled on M5Stick devices but an SD Card reader must be built and attached to the front panel pin header.
* EVIL Portal is only for use on professional engagements with a valid scope of work, educational or demonstration purposes. Storage, sale, or use of personal information without consent is against the law. 🤓

## BadUSB
**The content of the file isn`t supposed to be parsed like flipper!**

To choose a payload for the BadUSB on Cardputer instead of getting rickrolled, you need to create a file on the SD card root directory called "badpayload.txt".
This will be the raw payload that will be sent when the Cardputer is connected via USB cable.

By default, when you press the BadUSB option, it will send a Win + R key input and paste your payload, the content on the .txt file **can be a powershell one-liner**.


## Contributing
Go make your contributions on the main Bruce GitHub


## References
https://github.com/spacehuhn/ArduinoPcap

https://github.com/n0xa/m5stick-nemo

https://github.com/m5stack/M5Cardputer

https://github.com/caioluders/DPWO
