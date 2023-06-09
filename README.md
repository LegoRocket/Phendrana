# Phendrana
Repository for the Phendrana Keyboard - a split keyboard based on the nrf52840 and ZMK
## Photo
![Photo1](/Photos/20230405_115505.jpg)
## Demo Video

[![PhendranaDemoVideo](https://img.youtube.com/vi/Mj67zJ9yEYU/0.jpg)](https://youtu.be/Mj67zJ9yEYU)

## Features
- Longer Battery Life
- Multiple Bluetooth Connections
- Single-colour Backlight
- Cherry MX and Kailh Choc compatible
- Hotswap Switches, Battery, and MCU

## Firmware
Firmware can be found [here:](https://github.com/LegoRocket/Phendrana-ZMK)

### Compiling
To compile firmware for Phendrana:

Before flashing, ensure the .UF2 bootloader is installed. It should be version 0.7.0, which can be downloaded [here](https://github.com/adafruit/Adafruit_nRF52_Bootloader/releases/tag/0.7.0)
- The file should be named "nrf52840_m2_bootloader-0.7.0_s140_6.1.1.hex", if the M.2 is bought seperately, you will need the [Makerdiary Developer Kit Dock](https://makerdiary.com/products/nrf52840-m2-developer-kit) to upload it
1. Download the Phendrana Firmware repo
2. Follow the [ZMK Toolchain Setup](https://zmk.dev/docs/development/setup) Guide Local Build Guide
3. Place the Phendrana files in the zmk/app/boards/shields/phendrana folder (you will need to make the folder)
  - It should look like below:

![Screenshot 2023-04-06 165659](https://user-images.githubusercontent.com/31601733/230492485-16127788-ba0f-4520-8b1a-653b06c67110.png)

4. Open the zmk/app folder in terminal
5. Use the command "west build -b -p nrf52840_m2 -- -DSHIELD=phendrana_left" to build the left half firmware
6. Use the command "west build -b -p nrf52840_m2 -- -DSHIELD=phendrana_right" to build the right firmware
7. Upload both firmwares, to their respective halves, attempt to powerup at a similar time (The halves should automatically connect to each other)

## Inspirations
- [The Sanctuary](https://github.com/LegoRocket/Sanctuary-Keyboard-Hardware)
- [ZMK](https://zmk.dev/)
- [Quefrency](https://keeb.io/collections/quefrency-split-staggered-65-keyboard)

## Hardware Files

Currently the Hardware files are not released. The 3d case files are intended to be released at one point, however I wish to fix the files first, and provide more files for different versions of Phendrana.

KiCAD/Gerber files likely won't be released, and neither would the BOM. This is because it wasn't really designed to be built by others, and I'd want to do a complete overhaul if others were to build one. If you'd like Phendrana, contact me

## Versions
Rev 1.0.0 - Initial Release - Small errors, requiring 1 wire for USB connection, as well as other small wires to fix small trace errors

## Socials
#### [- Linktree:](https://linktr.ee/Lego_Rocket)
#### [- Youtube:](https://rebrickable.com/users/Lego_Rocket/)
#### [- Instagram:](https://www.instagram.com/lego_rocket_08/)


Note: This PCB was paid for by [PCBWay](https://pcbway.com/g/plrRz7), I was not paid beyond a free PCB, however if you'd like to support further projects, consider using the referral link 
