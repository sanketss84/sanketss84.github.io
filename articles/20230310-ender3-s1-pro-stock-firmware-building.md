# Ender 3 S1 PRO forked the stock firmware to add fixes and build locally 

Author: Sanket Sonavane   
Publish Date: 2023-03-10   
Last Updated: 2023-03-10  

The Ender 3 S1 PRO is based on Marlin and its source code is available on github , note you need to change to the `s1_pro` branch.
[CrealityOfficial/Ender-3S1 at s1_pro](https://github.com/CrealityOfficial/Ender-3S1/tree/s1_pro) 

I decided to fork this firmware and build my own locally so that I can add fixes and feature. This also helps me understand the build process. It was my first time building any 3d printer firmware on my own.

## tools needed to build marlin locally 
Marlin is the firmware which Creality used on the S1 PRO

- Microsoft Visual Studio Code 
- PlatformIO IDE extension for VS Code

once you have this you are all set to build marlin locally.

## fork the official github repo
Created a fork of the creality branch and add a few of my own branches for working with the firmware. 

- `s1_pro` 
    - should there be any future changes done to official branch will pull it here.
- `s1_pro_fixes` created from `s1_pro`
    - to add fixes by other users and commit them to my forked branch.
    - added fixes by pethical and kamoteshake which fixes the build issues
    - [Pull requests · CrealityOfficial/Ender-3S1](https://github.com/CrealityOfficial/Ender-3S1/pulls)
- `s1_pro_sanket`  created from `s1_pro`
    - to add fixes by other users and commit them to my forked branch.
    - add my own tweaks and features 

[sanketss84/Ender-3S1 at s1_pro](https://github.com/sanketss84/Ender-3S1/tree/s1_pro)
[sanketss84/Ender-3S1 at s1_pro_fixes](https://github.com/sanketss84/Ender-3S1/tree/s1_pro_fixes)
[sanketss84/Ender-3S1 at s1_pro_sanket](https://github.com/sanketss84/Ender-3S1/tree/s1_pro_sanket)

so after adding in all the fixes and commiting them I am able to build stock firmware successfully.

## references

reddit
- [these are pictures of the bed leveling at the two opposite ends of the lefts side of the bed The probe location in the second pic is much farther away from the edge. Is this normal? : Ender3S1](https://www.reddit.com/r/Ender3S1/comments/110zqqa/these_are_pictures_of_the_bed_leveling_at_the_two/)
  - here I had a discussion with reddit user kamoteshake about building stock firmware.

youtube
- [How To Update 3D Printer To Marlin 2.1 Firmware (for Ender 3 and more)](https://www.youtube.com/watch?v=dAlENiT3iek)
- [MARLIN - Essential Guide To Start Editing Your Own FIRMWARE](https://www.youtube.com/watch?v=ire4ZcAUsjA)
- [Beginner guide to editing Marlin firmware - step by step - UPDATE IN DESCRIPTION](https://www.youtube.com/watch?v=J9vxJT5Tgh4)
- [VSCODE - Edit Marlin Firmware - How To - Chris's Basement](https://www.youtube.com/watch?v=W6zYvRgGr3Q)
- [How to build Marlin Firmware Using VSCode easy way (2022)!](https://www.youtube.com/watch?v=vO9QmRr4gG4)
- [A Detailed (and Boring) Guide to Setting Up Marlin Firmware Using VSCode](https://www.youtube.com/watch?v=QXkqhf_JDSk)

