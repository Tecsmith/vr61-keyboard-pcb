# VR60 PCB

> My first foray into building a full keyboard PCB.  This is very, very early WIP.

> But for now... here is my wish list / intent list as a "feature" list :)

## Features

- 60% form factor
    - design to be GH61/HK61 compatible *(fits most case and plate combos)*
    - also compatible with Anne Pro 2 case *(drop in QMK replacement for AP2)*
- QMK + VIA default f/w
    - wired only *(no wireless)*
    - default keymaps for Mac use
- STM32 Microcontroller
- USB-C *(left side)*
- ESD protection
- Hot-swap, 5 ping switch slots
- Per key RGB SMT (south)
    - extra RGB under space - for pudding keycaps / better QMK Matrix animations
    - extra LED under caps lock (north/offset?) - for caps-lock state
    - extra LED under bottom row last three (north/offset?) - for layer state indicator
- Underglow RGB - but as optional
- Spare GPIO slots for expansion *(e.g. RGB 1-wire extension, QMK speaker, etc.)*
- PCB mounted stabs compatibility
- Reset under space-bar = reset without disassembly
- Un-obstructive status LED(s) under space-bar
