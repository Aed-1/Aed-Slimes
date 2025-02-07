# Aed-Slimes
My design of PCB and case for NRF slime trackers 
![20241123_214346](https://github.com/user-attachments/assets/708f6ef8-cd18-47c9-825b-2c562208999a)
![20241123_214303](https://github.com/user-attachments/assets/8460e52c-1b9e-4b58-a8f8-70a5f3bf03ce)

![Fusion360_C9sX65qt6Q](https://github.com/user-attachments/assets/5c8d1222-c1eb-4f2e-8a42-11a9422d3dac)

![image](https://github.com/user-attachments/assets/a8214c0e-b0c2-4734-bced-8f14698762c0)
![image](https://github.com/user-attachments/assets/1ea32cd5-dd67-4dcc-884d-8e459584aa33)


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
  
- my PCB
  
- male 2.54mm header pins (https://www.aliexpress.com/item/1005005990753794.html?spm=a2g0o.order_list.order_list_main.84.53071802maORE3)
  
- LIR2450 coin battery (www.amazon.co.uk/N20-Rechargeable-Battery-LIR2450-Lithium/dp/B093141K7D)
  
- LIR2450 coin battery holder (https://www.aliexpress.com/item/32809235496.html?spm=a2g0o.order_list.order_list_main.17.53071802maORE3)
  
- 3d printed shit
  
- ebyte dongle (https://www.aliexpress.com/item/1005004262523219.html?spm=a2g0o.order_list.order_list_main.5.53071802maORE3) (MAKE SURE TO SELECT THE E104-BT5040U OPTION) __this is currently not avaliable on ali express, check the docs for extra information__ (https://docs.slimevr.dev/diy/smol-slime.html#dongles-ebytenordic)
  
- push buttons (https://www.aliexpress.com/item/32882161197.html?spm=a2g0o.order_list.order_list_main.34.53071802maORE3) (you can get either color it doesnt matter)
  
- straps (https://shop.slimevr.dev/products/official-slimevr-straps-v2) (buy according to the amount of trackers you have)
  
- you also need basic soldering gear and cutters

  
# Building Trackers

for right now there is no image/video guide so you will have to make do with text for now, sorry D:


__IF YOU DO NOT FOLLOW THIS ORDER OF INSTRUCTIONS THE PARTS WILL NOT FIT!!!!__

__MAKE SURE EVERYTHING EXCEPT THE BATTERY HOLDER IS SOLDERED ON THE SIDE WITH THE LOGO AND NAME OTHERWISE THE PINS WILL BE BACKWARDS AND THE TRACKER WONT WORK (i know this is obvious but it is something alot of people forget)__

1. Solder buttons onto the PCB, it is a very tight fit and you may need to bend the pins a little in order for them to go in properly, they may also be tilted a little after they go in which is fine as long as they are soldered in
 
2. Solder pin headers onto the PCB in whichever order you like

3. solder battery header on the PCB __make sure the battery isnt in until after you are done building to prevent accidental shorts__
 
4. now solder the supermini and IMU onto the board making sure the USB-C port is on the side with the silkscreen of it (some components near the pins at the top of the supermini are very small so be careful not to accidentally bridge them)
 
5. put battery in the battery holder and put the tracker into the case (might be a tight fit depending on which printer you used and its tolerences, just push on it and dont worry about the tracker snapping. you probably couldnt snap it if you tried.)

# prerequisite for firmware flashing

you will need to download the nRF Connect for desktop app as well as all the modules for it listed on this section of the docs:
https://docs.slimevr.dev/diy/smol-slime.html#software

# Updating Bootloader
___YOU WILL NEED TO DO THIS BEFORE UPLOADING FIRMWARE ON TRACKERS OTHERWISE YOU RISK BRICKING YOUR TRACKERS___

follow the guide below on all of your trackers:
https://docs.slimevr.dev/diy/smol-slime.html#updating-adafruit-bootloader-supermini--xiao

# Flashing Tracker Firmware

Follow this guide on uploading firmware to your trackers, only difference is that you need to make sure you upload the "Zephyr.uf2" file in the Firmware folder in this github repo instead of the one mentioned in the guide:
https://docs.slimevr.dev/diy/smol-slime.html#supermini-and-other-devices-with-adafruit-bootloader-as-receivertracker

# Flashing Dongle Firmware

Now you can follow this guide below to upload the firmware for your dongle, only difference is to use the "Zephyr.hex" file in the Firmware folder in this github repo instead of the one mentioned in the guide:
https://docs.slimevr.dev/diy/smol-slime.html#dongles-ebytenordic

# What next?

Now you will need to follow the slimevr docs listed below in order to pair your trackers to your reciever as well as calibrate them:
https://docs.slimevr.dev/diy/smol-slime.html#pairing-mode

# FAQ (Frequently asked questions)

Q: "what IMUs can i use?"

A: currently there are 3 main IMUs you can choose from, for a low budget you can use LSM6DSR (https://store.kouno.xyz/products/lsm6dsr-ist8306-module), and if you have a high budget you can either get the ICM-45686 (https://store.kouno.xyz/products/icm-45686-ist8306-module) or the LSM6DSV (https://moffshop.deyta.de/products/lsm6dsv-module)

# Extra informatiom

SW0 is set to pin 31, this info is useful if you decide to mess around with the firmware and build it yourself

CASE DIMENSIONS: 35.20x37.04x19

STRAP LOOP DESIGNED BY PIXEL (pixel_lily on discord)


