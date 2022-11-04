# VR61 - MicroMod 60% Custom Keyboard PCB

***Featuring SparkFun's MicroMod Processor Boards***

---

> Very happy to announce that [PCBWay](https://pcbway.com) has gratefully sponsored the production of the first 5 RevA PCBs, and a partial assembly service *(all but the USB-C, Hot-Swap Sockets, JST-ph4 & SK6812's)*, for this project.  *(I will post images and results of the prototype testing [herein](docs/updates/readme.md) as I progress.)*
>
> [![Official Sponsor - PCBWay](docs/pcbway.jpg)](https://pcbway.com/)
>
> Thank you [PCBWay](https://pcbway.com/)!

Please follow the updates to this production process on the [updates](docs/updates/readme.md) page.

---

![PCB Top View](docs/vr61-pcb-top.png)

![PCB Bottom View](docs/vr61-pcb-btm.png)

Published as Open Source, under [MIT License](LICENSE.md):

- Rev A
    > Do not use this revision, it has terminal flaws.

    * ~~[PDF Schematic](docs/vr61-revA.pdf)~~
    * ~~[EAGLE PCB](EAGLE/vr61/vr61-revA.brd)~~
    * ~~[EAGLE Schematic](EAGLE/vr61/vr61-revA.sch)~~

- Rev B
    > **WORKING, OK TO BUILD**
    * [PDF Schematic](docs/vr61-revB.pdf)
    * [EAGLE PCB](EAGLE/vr61/vr61-revB.brd)
    * [EAGLE Schematic](EAGLE/vr61/vr61-revB.sch)

*(Interim)* QMK code:
* https://github.com/Tecsmith/vr61-keyboard-qmk
* *Subject to change for Rev B build.*
* USB Identifier registered with [pid.codes](https://pid.codes/) = [`1209`/`7672`](https://pid.codes/1209/7672/)

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
        - ***NB:*** *Cannot get the LED's to work on this, but the key matrix works just fine* ![Help Wanted](https://img.shields.io/badge/HELP-WANTED-brightgreen)

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

   ... e.g., add speaker

- Both `[Reset]` and `[Boot]` buttons *(as per MicroMod ref. design)*

    ... plus under space-bar Boot pins for bootload without disassembly *(press while inserting cable for bootloader function)*

## Progression / Variants

- **VR61 Rev B**
    - Keymap Working on both STM32 and PR2040
    - LED's Working on STM32 *(unresponsive on RP2040)*
    - *(Optional EEPROM not tested yet*

- ~~VR61 Rev A~~
    - [KLE link](http://www.keyboard-layout-editor.com/#/gists/c812c931186e45a5acbc3e217ef4f161)


---
Made with &#9829; - Vino Rodrigues
