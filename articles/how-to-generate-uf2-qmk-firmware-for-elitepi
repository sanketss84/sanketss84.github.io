## how to generate .uf2 qmk firmware 

So you recently picked a aurora series lily58 or corne or sweep and choose elite-pi as the microcontroller of choice for its higher memory compared to the elite-c and are wondering how to generate the uf2 boot file to be flashed to the elite-pi. This is the same query I faced so lets try to understand this step by step.


I suppose you dont have the QMK environment setup locally so we begin from there.

The QMK docs is a great place to start with the environment setup and there is no point in duplicating that information so I will directly link the pages here as those steps are identical to what you need to do.
 
1. [QMK Introduction](https://docs.qmk.fm/#/newbs)
2. [Setting Up Your QMK Environment](https://docs.qmk.fm/#/newbs_getting_started)
3. [Building Your First Firmware](https://docs.qmk.fm/#/newbs_building_firmware)
4. [Flashing Your Keyboard](https://docs.qmk.fm/#/newbs_flashing)

These doc pages give you a solid foundation.

NOTE
- these build steps are for the Aurora Sweep board.
- just replace the respective keyboard in the build command for your lily58 or corne

To generate the hex firmware file for elite-c the command is as follows
```bash
qmk compile -kb splitkb/aurora/sweep/rev1 -km default
```
the qmk_firmware is generated in this folder
C:\Users\<your-windows-username>\qmk_firmware
you shall find the .hex file here.

for elitepi
```bash
qmk compile -c -kb splitkb/aurora/sweep/rev1 -km default -e CONVERT_TO=elite_pi
```

the qmk_firmware is generated in this folder
C:\Users\<your-windows-username>\qmk_firmware
you shall find the .uf2 file here.
