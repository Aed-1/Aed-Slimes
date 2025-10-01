# Aed-Slimes
My design of PCB and case for NRF slime trackers 

<img class="caseImage"
    src=".\img\CasePhoto1.png" height="200">
<img class="caseImage"
    src=".\img\CasePhoto2.png" height="200">
<img class="caseImage"
    src=".\img\Fusion360_CaseImage.png" height="200">

<img class="caseImage"
    src=".\img\PcbImage1.png" height="200">
<img class="caseImage"
    src=".\img\PcbImage2.png" height="200">

# Ordering PCB

download the Aed_Slime_Gerber.zip file from the PCB folder on this repo

go to https://jlcpcb.com and follow the steps shown below

step 1
![image](https://github.com/user-attachments/assets/da5ba7ce-9062-42f9-9c0e-eb114254c943)

step 2

![image](https://github.com/user-attachments/assets/ceb41bb1-f61c-43fd-aea5-fd970abdbd00)

step 3

![image](https://github.com/user-attachments/assets/aed3eea8-19f6-40ea-b97f-e0caf3df63f8)

step 4

![image](https://github.com/user-attachments/assets/d31df2bc-610b-49ab-a04e-3f2d896ae61a)

step 5

![image](https://github.com/user-attachments/assets/9dabd1fd-3969-44dc-a874-b8fe2561994b)

step 6

![image](https://github.com/user-attachments/assets/c73b1f30-91ce-4276-a46e-35141785caad)

step 7

![image](https://github.com/user-attachments/assets/df0432a5-79c0-4957-8616-9c4eee1fb82e)

step 8

![image](https://github.com/user-attachments/assets/e3b38478-d046-4fcd-b2c1-c64a7df9fa44)


# Parts List

- SuperMini NRF52840 (https://www.aliexpress.com/item/1005007738886550.html?spm=a2g0o.order_list.order_list_main.11.53071802maORE3)
  
- IMU of your choice (refer to https://docs.slimevr.dev/diy/imu-comparison.html)
  
- the PCB
  
- male 2.54mm header pins (https://www.aliexpress.com/item/1005005990753794.html?spm=a2g0o.order_list.order_list_main.84.53071802maORE3)
  
- LIR2450 coin battery (EEMB version on amazon with welded pins)
  
- 3d printed cases and strap hooks
  
- holyIOT Dongle (can be found on aliexpress)
  
- push buttons (https://www.aliexpress.com/item/32882161197.html?spm=a2g0o.order_list.order_list_main.34.53071802maORE3) (you can get either color it doesnt matter)
  
- straps (https://shop.slimevr.dev/products/official-slimevr-straps-v2) (or any other 35mm wide strap) (buy according to the amount of trackers you have)
  
- you also need basic soldering gear, kapton tape and flush cutters

  
# Building Trackers

for right now there is no image/video guide so you will have to make do with text for now, sorry D:


__IF YOU DO NOT FOLLOW THIS ORDER OF INSTRUCTIONS THE PARTS MIGHT NOT FIT!!!!__

__MAKE SURE EVERYTHING EXCEPT THE BATTERY IS SOLDERED ON THE SIDE WITH THE LOGO OTHERWISE THE PINS WILL BE BACKWARDS AND THE TRACKER WONT WORK__

1. Solder buttons onto the PCB, it is a very tight fit and dont be afraid to bend the pins a little bit, if they snap off you always have replacements as these buttons usually come in packs of 50/100
 
2. Solder pin headers onto the PCB in whichever order you like

3. cut the pins on the underside of the pcb to make room for the battery

4. Stick kapton tape to bottom of PCB covering all pins apart from the 2 battery pins (this is not 100% necessary but is HIGHLY recomended as if you accidentally short the battery to the pins while in use or building it, you will fry your promicro board and risk a fire)
 
5. now solder the supermini and IMU onto the board making sure the USB-C port is on the side with the silkscreen of it (some components near the pins at the top of the supermini are very small so be careful not to accidentally bridge them)

6. solder battery on the PCB making sure the positive and negative terminals match accordingly
 
7. Finally, put the tracker into the case (might be a tight fit depending on which printer you used and its tolerences, just push on it and dont worry about the tracker snapping. you probably couldnt snap it if you tried.)


# prerequisite for firmware flashing

you will need to download the nRF Connect for desktop app as well as all the modules for it listed on this section of the docs:
https://docs.slimevr.dev/diy/smol-slime.html#software

# Updating Bootloader
___YOU WILL NEED TO DO THIS BEFORE UPLOADING FIRMWARE ON TRACKERS OTHERWISE YOU RISK BRICKING YOUR TRACKERS___

Download the bootloader with the below link and flash by putting tracker into DFU mode and dragging the .uf2 file into the drive that appears:
https://github.com/SlimeVR/Adafruit_nRF52_Bootloader/releases/download/0.9.2-SlimeVR.7/update-slimenrf_promicro_bootloader-0.9.2-SlimeVR.7_nosd.uf2

# Flashing Tracker Firmware

Follow this guide on uploading firmware to your tracker
https://docs.slimevr.dev/smol-slimes/firmware/smol-flashing-firmware.html#flashing-the-firmware-using-uf2

# Flashing Dongle Firmware

Now you can follow this guide below to upload the firmware for your dongle
https://docs.slimevr.dev/smol-slimes/firmware/smol-flashing-firmware.html#flashing-dongles-with-softdevicenordic-bootloader-ebytenordic

# What next?

Now you will need to follow the slimevr docs listed below in order to pair your trackers to your reciever as well as calibrate them:
https://docs.slimevr.dev/smol-slimes/firmware/smol-pairing-and-calibration.html


# Extra informatiom
if pressing the buttons make the tracker move around in the case you can reprint the tracker in a filament that doesnt deform easily or hot glue it into place, either option works but hot glue wont look as good

CASE DIMENSIONS: 35.20x37.04x15mm

STRAP LOOP DESIGNED BY PIXEL (pixel_lily on discord)


