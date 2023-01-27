# IRIS Vs Lily Vs Sofle 
Author: Sanket Sonavane   
Publish Date: 2023-01-27  
Last Updated: 2023-01-27  

NOTE: This article is a work in progress and has my latest thoughts documented.

## summary
sofle v2 :P

## why sofle v2 > lily58 pro > iris rev7
It started with the IRIS group buy  but as I started digging in to better understand the board I started seeing some shortcomings and also found that there are boards which might be more modular and flexible for my needs. this is what made me research lily 58 pro and then lead to sofle.

## problems with iris 
- importing this is costly as we need to get the pcb from keebio
- closed source 
- 54~56 keys based on how you do your thumb stack thats less keys than lily which is 58 keys
- the microcontroller is soldered on the board, I prefer socketed microcontroller leaves room for swapping it out. 

## lily58 vs sofle
- while lily58 is a good design with 58 keys sofle added 2 more keys 
- sofle (6×4+5 keys column-staggered split keyboard with encoder support) was created by Josef Adamčík 
	- based on Lily 58 Pro , Corne and Helix
- the lowered pinky keys placement and thumb cluster placement which is more to the left on the sofle v2 is a better design.

> Lily 58 was also not built from scratch. In its licence file its written that it’s derived from [Helix](https://github.com/MakotoKurauchi/helix "Helix keyboard"), [Ergo42](https://github.com/Biacco42/Ergo42 "Ergo42 keyboard") and [Corne AKA crkbd](https://github.com/foostan/crkbd "Corne Keyboard AKA crkbd") (which was also called Helidox and is based on Helix).

## sofle codebase for QMK
- Josef Adamcik used Lily 58 Pro as reference and cleaned all the code
- so this is a much more streamlined and efficient code base which get rids of bits that are old or deprecated

> PS I havent checked the code base myself yet.

[qmk_firmware sofle](https://github.com/qmk/qmk_firmware/tree/master/keyboards/sofle) 
[qmk_firmware lily58](https://github.com/qmk/qmk_firmware/tree/master/keyboards/lily58)

## sofle v1 to v2
- SofleV1 was created as an improvement over Lily58 by adding two additional keys to the PCB and supports MX and choc hotswap sockets
- SofleV2 was created as from scratch PCB over V1 and has updated the thumb and pinky finger placement but got rid of choc hotswap sockets and supports only MX hotswap
- SofleV2 RGB was created by a community member as scratch PCB to add RGB to the board
- SofleV2 Choc HotSwap was created by another community member as scratch PCB 

## sofle v2 community contributions
- Sofle V2 (MX hotswap only) by Josef Adamcik (original)
    - [Sofle Keyboard - build guide (v1/v2) - SofleKeyboard](https://josefadamcik.github.io/SofleKeyboard/build_guide.html)
- Sofle V2 RGB by Dane Evans (designed from scratch) 
    - [Sofle Keyboard - build guide (RGB) - SofleKeyboard](https://josefadamcik.github.io/SofleKeyboard/build_guide_rgb.html)
- Sofle V2 low profile by Brian Low (designed from scratch)
    - [Sofle Keyboard - build guide (Choc) - SofleKeyboard](https://josefadamcik.github.io/SofleKeyboard/build_guide_choc.html) 

There is also other variations 
- Sofle RGB by Keyhive its code is totally different and maintained by keyhive
- Kimiko [Search results for kimiko - Keycapsss](https://keycapsss.com/search?sSearch=kimiko) 

read more https://josef-adamcik.cz/electronics/another_year_for_sofle.html


## sofle v2 vs lily58 pro hand placement
to test your finger placement on these keyboards you can take a printout of these layout which are to scale on an A4 paper.
[Compare split keyboards](https://jhelvy.github.io/splitKbCompare/) 
- i applied following filters 
	- number of keys 54 to 61
	- number of rows 4 to 6
- use this link to generate PDF of sofle , lily58 , iris layout.
- ensure when you take a printout dont apply any form of scaling and print these on A4 paper.
- these are to scale printouts and they help you get a feel of how you fingers are placed on these various keyboards.
- check all your finger movements while touch typing especially your pinky and the thumb placement.

**PDF downloads**
- [iris a4 pdf to scale](/assets/pdf/compare_iris_A4.pdf)  
- [lily58 a4 pdf to scale](/assets/pdf/compare_lily58_A4.pdf)  
- [sofle v1 a4 pdf to scale](/assets/pdf/compare_sofle_v1_A4.pdf)  
- [sofle v2 a4 pdf to scale](/assets/pdf/compare_sofle_v2_A4.pdf)  
- [kimiko a4 pdf to scale](/assets/pdf/compare_kimiko_A4.pdf)  

## qmk configurator
[Sofle QMK Configurator](https://config.qmk.fm/#/sofle/rev1/LAYOUT)

## footnotes

## references
- Sofle Journey of Josef Adamčík
	- [Building a custom keyboard - Katana60 – Josef Adamčík](https://josef-adamcik.cz/electronics/buiding-a-custom-keyboard-katana60.html) 
		- [Extend Extra Extreme! - User contributions - Colemak forum](https://forum.colemak.com/topic/2014-extend-extra-extreme/)
	- [Corne keyboard – Josef Adamčík](https://josef-adamcik.cz/electronics/corne-keyboard-build-log.html) 
	- Part 1 [In search of the best custom keyboard layout – Josef Adamčík](https://josef-adamcik.cz/electronics/in-search-of-the-best-custom-keyboard-layout.html)
	- Part 2 [Let me introduce you SofleKeyboard - a split keyboard based on Lily58 and Crkbd – Josef Adamčík](https://josef-adamcik.cz/electronics/let-me-introduce-you-sofle-keyboard-split-keyboard-based-on-lily58.html)
	- Part 3 [SofleKeyboard build log/guide – Josef Adamčík](https://josef-adamcik.cz/electronics/soflekeyboard-build-log-and-build-guide.html)
	- Part 4 [Sofle Keyboard evolution: slow and not really steady – Josef Adamčík](https://josef-adamcik.cz/electronics/soflekeyboard-evolving.html)
	- Part 5 [Another year of Sofle keyboard – Josef Adamčík](https://josef-adamcik.cz/electronics/another_year_for_sofle.html)
- Sofle Keyboard
	- [SofleKeyboard - A split keyboard based on Lily58, Crkbd and Helix keyboards](https://josefadamcik.github.io/SofleKeyboard/) 
	- [josefadamcik/SofleKeyboard: A split keyboard based on Lily58, Crkbd and Helix keyboards](https://github.com/josefadamcik/SofleKeyboard)
	- [qmk\_firmware/keyboards/sofle at master · qmk/qmk\_firmware](https://github.com/qmk/qmk_firmware/tree/master/keyboards/sofle) qmk sofle codebase and keymaps
- Lily58 Keyboard
	- [kata0510/Lily58: 6×4+4keys column-staggered split keyboard.](https://github.com/kata0510/Lily58) github
	- [Lily58/buildguide\_en.md at master · kata0510/Lily58](https://github.com/kata0510/Lily58/blob/master/Pro/Doc/buildguide_en.md) build guide english
	- [Lily58/buildguide\_en.md at master · kata0510/Lily58](https://github.com/kata0510/Lily58/blob/master/Pro/Doc/buildguide_en.md) qmk lily58 codebase and keymaps