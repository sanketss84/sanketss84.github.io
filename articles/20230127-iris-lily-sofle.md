# IRIS Vs Lily Vs Sofle 
Author:  Sanket Sonavane
Publish Date: 2023 01 27
Last Updated: 2023 01 27

NOTE: This article is a work in progress and has my latest thoughts documented.

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

## sofle v1 to v2
- SofleV1 was created as an improvement over Lily58 by adding two additional keys to the PCB and supports MX and choc hotswap sockets
- SofleV2 was created as from scratch PCB over V1 and has updated the thumb and pinky finger placement but got rid of choc hotswap sockets and supports only MX hotswap
- SofleV2 RGB was created by a community member as scratch PCB to add RGB to the board
- SofleV2 Choc HotSwap was created by another community member as scratch PCB 

## sofle v2 community contributions
- Sofle V2 (MX hotswap only) by the Josef Adamcik
- Sofle V2 RGB by Dane Evans (designed from scratch) 
- Sofle V2 low profile by Brian Low (designed from scratch)

## footnotes
- [Building a custom keyboard - Katana60 – Josef Adamčík](https://josef-adamcik.cz/electronics/buiding-a-custom-keyboard-katana60.html) 
- [Corne keyboard – Josef Adamčík](https://josef-adamcik.cz/electronics/corne-keyboard-build-log.html) 
* Sofle Journey of Josef Adamčík
	* Part 1 [In search of the best custom keyboard layout – Josef Adamčík](https://josef-adamcik.cz/electronics/in-search-of-the-best-custom-keyboard-layout.html)
	* Part 2 [Let me introduce you SofleKeyboard - a split keyboard based on Lily58 and Crkbd – Josef Adamčík](https://josef-adamcik.cz/electronics/let-me-introduce-you-sofle-keyboard-split-keyboard-based-on-lily58.html)
	* Part 3 [SofleKeyboard build log/guide – Josef Adamčík](https://josef-adamcik.cz/electronics/soflekeyboard-build-log-and-build-guide.html)
	* Part 4 [Sofle Keyboard evolution: slow and not really steady – Josef Adamčík](https://josef-adamcik.cz/electronics/soflekeyboard-evolving.html)
	* Part 5 [Another year of Sofle keyboard – Josef Adamčík](https://josef-adamcik.cz/electronics/another_year_for_sofle.html)