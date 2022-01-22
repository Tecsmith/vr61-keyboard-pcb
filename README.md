# VR60 *"Goldilocks"* PCB

> &#x26A0; BUCKET LIST PROJECT - not currently under development &#x26A0;

> My first foray into building a full keyboard PCB.  This is very, very early WIP.

> But for now... here is my wish list / intent list as a "feature" list :)

## Features

- 60% form factor
    - design to be GH61/HK61 compatible *(fits most case and plate combos)*
    - also compatible with Anne Pro 2 case *(drop in QMK replacement for existing AP2's)*
- QMK + VIA default f/w
    - wired only *(no wireless)*
    - default keymaps for Mac use
- STM32 Microcontroller
- USB-C *(left side)*
- ESD protection
- Hot-swap, 5 ping switch slots
- PCB mounted stabs compatibility
- 1.25, 1.25, 1.25, 6.25, 1.25, 1.25, 1.25, 1.25 bottom row
- Per key RGB SMT (south)
    - WS2812 or APA102 driver
    - extra RGB under space - for pudding keycaps / better QMK Matrix animations
    - extra LED under caps lock (north/offset?) - for caps-lock state
    - extra LED under bottom row last three (north/offset?) - for layer state indicator
- Underglow RGB - but as optional *(solder off 0ohm trace switch)*
- Spare GPIO slots for expansion *(e.g. RGB 1-wire extension, QMK speaker, etc.)*
- Two reset buttons
    - under space-bar = reset without disassembly
    - bottom of PCB as per normal in case plate covers the space-bar one
- Layer selector toggle switch in the slot where the AP2 has its wifi-switch - so can be used as a Keychron-esque DIP switch
- Un-obstructive (tiny) status LED(s) under space-bar (next to reset) and near UPB port
