# VR61 - MicroMod 60% Custom Keyboard PCB

***Featuring SparkFun's MicroMod Processor Boards***

---

> Very happy to announce that [PCBWay](https://pcbway.com) has gratefully sponsored the production of the first 5 RevA PCBs, and a partial assembly service *(all but the USB-C, Hot-Swap Sockets, JST-ph4 & SK6812's)*, for this project.
>
> [![Official Sponsor - PCBWay](docs/pcbway.jpg)](https://pcbway.com/)
>
> Thank you [PCBWay](https://pcbway.com/)!

Please follow the updates to this production process on the [changelog](CHANGELOG.md) page.

---

![PCB Top View](docs/vr61-pcb-top.png)

![PCB Bottom View](docs/vr61-pcb-btm.png)

Published as Open Source, under a [ Creative Commons Share-alike 4.0 International](LICENSE.md).  [![CC-0 license](https://shields.io/badge/-BY--SA_4.0-black?logo=creativecommons&logoColor=%23000&labelColor=%23c1c1c1
)](https://creativecommons.org/licenses/by-sa/4.0/)


### **Rev B** &nbsp; ![](https://shields.io/badge/OK-Working-green?logo=checkmarx&OK=Working)

> &#128077; **WORKING, OK TO BUILD**

* [PDF Schematic](docs/vr61-revB.2.pdf) <sup>1</sup>
* [EAGLE PCB](EAGLE/vr61/vr61-revB.brd)
* [EAGLE Schematic](EAGLE/vr61/vr61-revB.sch)

* Notes:
    - Keymap Working on both STM32 and PR2040
    - *(Optional EEPROM not tested yet)*

> <sup>1</sup> = *RevB.1 schematic is [here](docs/vr61-revB.pdf)*

### **Rev A** &nbsp; ![](https://img.shields.io/badge/!!-Fails-critical)

> &#9888; Do not use this revision, it has terminal flaws.

* ~~[PDF Schematic](docs/vr61-revA.pdf)~~
* ~~EAGLE PCB~~ <sup>2</sup>
* ~~EAGLE Schematic~~ <sup>2</sup>

> <sup>2</sup> = *to access these files please use the Github history*


### QMK code:

* https://github.com/Tecsmith/vr61-keyboard-qmk
* USB Identifier registered with [pid.codes](https://pid.codes/) = [`1209`/`7672`](https://pid.codes/1209/7672/)

### Layout

* [KLE link](http://www.keyboard-layout-editor.com/#/gists/c812c931186e45a5acbc3e217ef4f161)


*****

## Features

**VR61-MicroMod** - using SparkFun MicroMod STM32 or RP2040 M.2 module

### Core Design Elements

- 60% form factor
    - Design to be compatible with GH60/HK60 cases
    - Also compatible with Anne Pro 2 cases *(~~drop in~~ QMK replacement for existing AP2's or AP2 cases)* *[Removal of battery and minor case cut in the battery compartment required.]*
    - MicroMod positioned in case *"battery compartment"* space.

- QMK + VIA default f/w
    - Wired only *(no wireless)*
    - Default key-maps for Mac users

- User choice of microcontroller
    
    - [STM32 Processor](https://www.sparkfun.com/products/17713) 
        - ARM Cortex-M4, 168MHz, 1MB Flash, 192kB SRAM
        - https://github.com/Tecsmith/vr61-keyboard-qmk

    - [RP2040 Processor](https://www.sparkfun.com/products/17720) 
        - ARM Cortex-M0+, 133MHz, 128Mb Flash (16MB external), 264kB SRAM in six banks
        
- USB-C *(left side)*

    ... but also optional JST connector for [ai03 Unified C3 Daughterboard](https://github.com/ai03-2725/Unified-Daughterboard)

- ESD, Over Voltage and Over Current protection

    ... and cable shield noise filter

- Hot-swap, 5 pin switch slots

- PCB mounted stabs compatibility

- Dual ANSI / ISO layout support

- 61-Key (ANSI) / 62-Key (ISO) Layout [1.25, 1.25, 1.25, **6.25**, 1.25, 1.25, 1.25, 1.25] bottom row *(a.k.a. "Poker" / "POK3R" Layout)*

- Limited RGB LEDs *(SK6812 mini-E)*

    - RGB Caps Lock Indicator

    - North facing RGB's under the `5`, `6`, `7` & `8` keys for layer indicator

    - WS2812/SK6812 breakout for optional external LEDs

- Spare GPIO pins (`52` & `63`) breakout for expansion

   ... e.g., ~~add speaker~~

- Both `[Reset]` and `[Boot]` buttons *(as per MicroMod ref. design)*

    ... plus under space-bar Boot pins for bootload without disassembly *(press while inserting cable for bootloader function)*

---
Made with &#9829; by Vino Rodrigues
