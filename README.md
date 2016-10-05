Princeton Pi - 01 - NOOBS, Kodi, and whatever
=============================================

7:30 Wed, October 5, 2016, [Tiger Labs](http://tigerlabs.co)

These notes live [here](https://github.com/bhamail/princeton-pi-01.git). 
Written in the [Markdown](https://daringfireball.net/projects/markdown/syntax) format. 
Improvements are welcome! 

The Org
-------
The [Raspberry Pi Foundation](https://www.raspberrypi.org)

The Hardware
------------
[Newark](http://www.newark.com) or [MCM Electronics](http://www.mcmelectronics.com) or Amazon or others...

* Be sure you have a 2 amp (or 2.5 amp) usb power supply for the Pi3! 
[CanaKit](https://www.amazon.com/CanaKit-Raspberry-Supply-Adapter-Charger/dp/B00MARDJZ4) has a few bundles that include
such a power supply.

NOOBS
-----

*N*ew *O*ut *O*f *B*ox *S*oftware - https://www.raspberrypi.org/downloads/noobs/

Current version: 1.9.3, size: 1.17gb zip

OS's included:

  1. Raspbian - latest is based on [Debian](https://www.debian.org) [Jessie](https://www.debian.org/releases/stable/)
  1. LibreELEC_RPI2 - Kodi media player - https://libreelec.tv
  1. OSMC_PI2 - Open Source Media Center - https://osmc.tv
  1. Raspbian Lite - minimal install
  1. Windows 10 IoT - release or bleeding edge versions
  
[NOOBS Setup Videos](https://www.raspberrypi.org/help/videos/) - See "NOOBS SETUP"

* No need to deal with disk partitioning, etc. Just unzip, and copy all files onto DOS formatted SDCard.

  - During first boot, when selecting OS's to install, don't forget to change the local at the bottom of the screen
  from Great Britain to US, and same for the keyboard locale.

* Default userId: pi

* Default password: raspberry 

    - should probably change this
     
        - via [raspi-config](https://www.raspberrypi.org/documentation/configuration/raspi-config.md)
        - via Desktop UI -> Pi -> Preferences -> Raspberry Pi Configuration

* Connect to network

    - ethernet
    - wireless
    
  What's my Pi's IP Address:

      pi@raspberrypi:~ $ ifconfig

  Useful to ssh into your Pi.

* Update the Pi with latest OS patches.

  - via CLI (Command Line Interface)

        $ sudo apt-get update && sudo apt-get upgrade
      
  - via Desktop UI
  
      - Pi -> Preferences -> Add / Remove Software ->
      
        - Options -> Refresh Package Lists
        - Options -> Check for Updates
        
 * Yeah! [Chromium](https://www.chromium.org) web browser with hardware video acceleration for YouTube vids.
 
LibreELEC
---------

[LibreELEC](https://libreelec.tv) - Free/Open Source *E*mbedded *L*inux *E*ntertainment *C*enter

* "Just enough OS for [KODI](https://kodi.tv)"

  - KODI is an Open Source software media center
  - KODI was formerly known as XMBC (*X**B*ox *M*edia *C*enter)
  - KODI is available for just about any device (even Android phones)

* LibreELEC has Pi-optimized distro - and is included in NOOBS.

* First boot has setup wizard.

* You should also set your locale info:

  - System -> Settings -> Appearance -> International ->
   
     - Timezone country : United States
     - Timezone: America/New York

* System -> Addons -> 
 
   Video Addons
   
     - Nasa
     - PBS Think TV
     - TED Talks
     - YouTube

* Be aware of Settings "Level" - 'Basic' shows fewer settings, 'Standard' shows more, 
  'Advanced' and 'Expert' show more still...
  
* PVR plugin for use with a Media Server - like [MythTV](http://mythtv.org)
