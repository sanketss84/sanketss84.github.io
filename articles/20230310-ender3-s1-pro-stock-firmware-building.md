# Ender 3 S1 PRO forked the stock firmware to add fixes and build locally 

Author: Sanket Sonavane   
Publish Date: 2023-03-10   
Last Updated: 2023-03-11  

The Ender 3 S1 PRO is based on Marlin and its source code is available on github , note you need to change to the `s1_pro` branch.
[CrealityOfficial/Ender-3S1 at s1_pro](https://github.com/CrealityOfficial/Ender-3S1/tree/s1_pro) 

I decided to fork this firmware and build my own locally so that I can add fixes and feature. This also helps me understand the build process. It was my first time building any 3d printer firmware on my own.

NOTE: These source code are based on v2.0.8.24 of the stock firmware.

## tools needed to build marlin locally 
Marlin is the firmware which Creality used on the S1 PRO

- Microsoft Visual Studio Code 
- PlatformIO IDE extension for VS Code

the marlin docs covers this development setup very well. 
[Installing Marlin (PlatformIO with VSCode) | Marlin Firmware](https://marlinfw.org/docs/basics/install_platformio_vscode.html)

once you have this you are all set to build marlin locally.

## few things to know before you build the stock firmware
- what's your current firmware 
- what's your controller board , mines STM32F401

these things need to be checked if set correctly or need to be tweaked in the firmware code before you flash this to your printer and risk bricking it.

## fork the official github repo
Created a fork of the creality branch and add a few of my own branches for working with the firmware. 

- `s1_pro` 
    - should there be any future changes done to official branch will pull it here.
- `s1_pro_fixes` created from `s1_pro`
    - to add fixes by other users and commit them to my forked branch.
    - added fixes by pethical and kamoteshake which fixes the build issues
    - [Pull requests · CrealityOfficial/Ender-3S1](https://github.com/CrealityOfficial/Ender-3S1/pulls)
- `s1_pro_sanket`  created from Creality official `s1_pro`
    - to add fixes by other users and commit them to my forked branch.
    - building for STM32F401 vs stock which has this config for STM32F103
        - refer this commit to make the necessary changes [Environment for STM32F401 · Pethical/Ender-3S1@2230852](https://github.com/Pethical/Ender-3S1/commit/22308521e74d386ac8c9e25f83337c9c045fb4a6) 
    - add my own tweaks and features 
        - refer these branches for changes that can be accomodated 
            - [Commits · Pethical/Ender-3S1](https://github.com/Pethical/Ender-3S1/commits/s1_pro_pethical)
            - [Commits · kamoteshake/Ender-3S1](https://github.com/kamoteshake/Ender-3S1/commits/s1_plus)
        - update the bed levelling grid to 6x6 or 5x5 from stock 4x4 for more accurate mesh creation.

my github branches
- [sanketss84/Ender-3S1 at s1_pro](https://github.com/sanketss84/Ender-3S1/tree/s1_pro)
- [sanketss84/Ender-3S1 at s1_pro_fixes](https://github.com/sanketss84/Ender-3S1/tree/s1_pro_fixes)
- [sanketss84/Ender-3S1 at s1_pro_sanket](https://github.com/sanketss84/Ender-3S1/tree/s1_pro_sanket)

so after adding in all the fixes and committing them I am able to build stock firmware successfully.

## still need to figure out
While I have so far figured out how to generate firmware for the controller board I haven't figured out how to 

- build firmware for stock touch display.
- build firmware for alternate display should I want to swap them on my s1 pro.
    - the ender 3 s1 display which was a nice color display but not touch screen and had a knob.
    - the classic 12864 display for ender 3 with a knob. 
    - bigtreetech 12864 display. 
    - the different displays might unlock more features which are still not available on the touch display
- build firmware for alternate touch probes.
- upgrade the entire controller board if need be and build firmware for it.

these are some cool things that I need to explore for future upgrades 

## references

reddit
- [these are pictures of the bed levelling at the two opposite ends of the lefts side of the bed The probe location in the second pic is much farther away from the edge. Is this normal? : Ender3S1](https://www.reddit.com/r/Ender3S1/comments/110zqqa/these_are_pictures_of_the_bed_leveling_at_the_two/)
  - here I had a discussion with reddit user kamoteshake about building stock firmware.

youtube
- [How To Update 3D Printer To Marlin 2.1 Firmware (for Ender 3 and more)](https://www.youtube.com/watch?v=dAlENiT3iek)
- [MARLIN - Essential Guide To Start Editing Your Own FIRMWARE](https://www.youtube.com/watch?v=ire4ZcAUsjA)
- [Beginner guide to editing Marlin firmware - step by step - UPDATE IN DESCRIPTION](https://www.youtube.com/watch?v=J9vxJT5Tgh4)
- [VSCODE - Edit Marlin Firmware - How To - Chris's Basement](https://www.youtube.com/watch?v=W6zYvRgGr3Q)
- [How to build Marlin Firmware Using VSCode easy way (2022)!](https://www.youtube.com/watch?v=vO9QmRr4gG4)
- [A Detailed (and Boring) Guide to Setting Up Marlin Firmware Using VSCode](https://www.youtube.com/watch?v=QXkqhf_JDSk)

