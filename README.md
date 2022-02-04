# VR60 *"Goldilocks"* PCB

> &#x26A0; BUCKET LIST PROJECT - not currently under development &#x26A0;

> My first foray into building a full keyboard PCB.  This is very, very early WIP.

> But for now... here is my wish list / intent list as a "feature" list :)

## Features

### Core design elements

- 60% form factor
    - Design to be GH60/HK60 compatible *(fits most case and plate combos)*
    - Also compatible with Anne Pro 2 case *(drop in QMK replacement for existing AP2's)*
- QMK + VIA default f/w
    - Wired only *(no wireless)*
    - Default key-maps for Mac use
- STM32 Microcontroller  ***(possibly with removable M.2 module)***
- USB-C *(left side)*
- ESD protection, over voltage and over current protection
- Hot-swap, 5 pin switch slots
- PCB mounted stabs compatibility
- 1.25, 1.25, 1.25, 6.25, 1.25, 1.25, 1.25, 1.25 bottom row
- Per key RGB SMT *(NORTH)*
    - *(Yes, north because it's more compatible with shine-through caps and I don't buy GMK anyway)*
    - WS2812 or APA102 driver
    - Extra RGB under space - for pudding keycaps / better QMK Matrix animations
    - Extra LED under caps lock (north/offset?) - for caps-lock state
    - Extra LED under bottom row last three (north/offset?) - for layer state indicator
- Under-glow RGB - but as optional *(solder off 0ohm trace switch)*
- Spare GPIO slots for expansion *(e.g. RGB 1-wire extension, QMK speaker, etc.)*
- Two reset buttons
    - Under space-bar = reset without disassembly
    - Bottom of PCB as per normal in case plate covers the space-bar one
- Layer selector toggle switch in the slot where the AP2 has its wifi-switch - so can be used as a Keychron-esque DIP switch
- Un-obstructive (tiny) status LED(s) under space-bar (next to reset) and near UPB port
- Additional EEPROM chip for larger VIA layer support

### Edge experiments

- Embedded ESP8266 or EP32 chip for over-wifi key-mapping
- Support for Logitec Unifying Reciever *(how???)*

## Possible design aids

- [GH60](https://github.com/komar007/gh60), also [read this](http://blog.komar.be/gh60-evolution/)
- Closest is the BM60 Poker - but that's not open source.
- [Bakeneko 60](https://github.com/kkatano/bakeneko-60)
- [Voyager 60](https://github.com/ai03-2725/Voyager60)
- [Plain6-C](https://github.com/evyd13/plain60-c)
- *(a bit off the design footprint)* [Grabert KB](https://github.com/KoBussLLC/grabert-hardware)
- for M.2 see https://github.com/makerdiary/python-keyboard
