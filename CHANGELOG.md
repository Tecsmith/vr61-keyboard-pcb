# Updates
All notable updates to this project will be documented in this file.

*(The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).)*

> [PCBWay](https://pcbway.com) graciously offered to sponsor the prototype build of this keyboard

<p align="center">
<a href="https://pcbway.com/"><img src="docs/pcbway.jpg"></a>
</p>

---

# Rev B - History

## 2024-09-17

> *a.k.a.* **Rev B.2**

### Added

- 4-pin DIP switch
  - 1..3 consume empty switch slots.
  - 4 is the VIN sensor switch for the MicroMod
- 3x Manufacturing fiduciary marks
- Expanded options for solder-on, or Mill-Max socket switches *(does not use hot-swap sockets)*
  - Split Right Shift
  - Split Backspace
  - Stepped Caps-Lock
- Added PCB edge slots to support Bakeneko type cases

### Changed

- Licence changed from MIT to [CC BY-SA 4.0](LICENCE.md) in compliance with the SparkFun MicroMod Licence.
- Maved to latest footprints of the Tecsmith [`ts-eagle-lib`](https://github.com/Tecsmith/ts-eagle-lib) keyboard library
  - MX key
  - MX Stabs
  - SK6821 LED
- Taces now route to socket via pads, not SMD hotswap pads as these may tear off in a desoldering scenario.
- Ajusted Ground Plane mesh/hash as former model had differeing setting for top and bottom
- Revised Boot button.  *(MicroMod provides 2 button reset/boot but both are ground based, so can be consolodated into one.)*

## 2022-08-30

- Placed order with PCBWay ... added Micromod and USB connector to this assembly set

## 2022-09-1

- PCBWay confirmed sourcing of all parts
- Order paid and go-ahead given

## 2022-10-17

- PCBWay order of 5 prototype bards arrived.  Some issues were encountered with the `74AHCT1G125GW` module footprint.

## 2022-10-23

- First prototype fully built
- Code implemented, but no success of getting the LED's to work

## 2022-10-27

- Finally got the LED's to work
- Issue was with the code and the PWM settings of the STM32 processor
- Cannot get the PR2040 code to work -- parking the RP2040 LED implementation, the keymap works however

## 2022-10-30

- Final code on the keymaps completed
- Minor edits to the PCB

## Pending

- PR2040 LED not working yet
- SPI EEPROM not tested *(not even attempted, yet)*

---

# Rev A - History

## 2022-06-17

- Order placed with PCBWay and confirmation received.


## 2022-06-28

### Finished goods photos sent

- Got an email will the finished build - shipping to me next.
  
  <a href="docs/updates/prod_1.jpg"><img src="docs/updates/prod_1.jpg" width="10%"></a>
  <a href="docs/updates/prod_2.jpg"><img src="docs/updates/prod_2.jpg" width="10%"></a>
  <a href="docs/updates/prod_3.jpg"><img src="docs/updates/prod_3.jpg" width="10%"></a>
  <a href="docs/updates/prod_4.jpg"><img src="docs/updates/prod_4.jpg" width="10%"></a>
  <a href="docs/updates/prod_5.jpg"><img src="docs/updates/prod_5.jpg" width="10%"></a>


## 2022-07-15

### PCB delivered

- Arrived in Sydney via DHL.  No issues.


## 2022-07-18

### Initial testing

- Soldered on UBS connector
- Soldered on MicroMod connector
- Installed SMT32 module and Tested key matrix - ***IT WORKS!***
  - Must say I build 2 boards and both didn't work at first - fault finding lead to discovery that one of the USB data lines was grounded.  On one board I stripped out the ESD thinking that was up-side-down... it wasn't.  And then I found it.  A solder short on the MicroMod connector between pin 5 and 7... on BOTH!
  - Must also say the soldering that Micromod connector was super difficult!
  - Next time I will have all the components installed by the supplier!
- PCBWay did an amazing job on the PCB!

## 2022-07-20

### Declaring Rev A as FAILED :(

Came across some terminal issues when compiling the code and attempting to retro-fit the PCB into a AnnePro2 case.

- The `ESC` key is off to right by 1mm.  Checked the CAD `.sch` and say that somehow I'd moved it and missed that it was off by 1mm.  Must have been on the rotation and I didn't double check.
- The LED implementation does not work electronically.  Somewhere between the MCU the Level Shifter and the first LED something happens and I blow the 1st LED.  Soldered on 3 replacements, all blown. Bypass the `Caps-Lock` position and made `5` key 1st - that blew to.  Need to relook at more ref. designs for this.

#### Next

- Everything else seems to work.  Code also works...
- ... but I'd assumed the memory IC on the MicroMod was an EEPROM. **It's not** .. it's Flash! *(Rookie assumption!)*  Will implement an I²C EEPROM as the 100,000 write cycles of the W25Q32FV Flash is far, far less than the 4,000,000 of an external EEPROM like the ST M24Cx IC's.
> Wondering what I can do with the Flash tho ... seems a waste.

---

# Rev A - Issues
> as discovered ... to implement in rev. B

- [ ] ~~Position of MicroMod connector is too low, does not fit in AP2 case without minor cutting - possibly move this up as far as it can go.~~ *[Cannot move as it will interfere with key]*
- [x] Position of the BOOT pads in the space bar area should align to the AP2 slot
- [x]  Spacing of key was generated by [Kalerator](https://kalerator.clueboard.co/) ... but this generator spaces the keys at 19mm.  **However***... spacing for keyboards is **19.05mm**!

#### Post FAIL / Rev B WIP

- [x] Correct `ESC` key position
- [x] New LED / Level Shift design
- [ ] ~~Bring out I²C from Micromod~~ *[I²C not usable as pins are shared with matrix pins for PR2040 module]*
- [x] ~~Add I²C EEPROM module~~ *[Changed this to SPI]*
- [x] Move USB 0.5mm right to align to AP2 case slot. *(Uncertain this will jeopardise the GH60 cases.)*

## Maybe

- [x] Move 5678 LED's to north-facing.
- [x] Possibly incorporate a ISO layout?
- [ ] ~~Possibly incorporate a 64-key layout?~~ *[Does not fit]*

> Rev B is ready *[26 Aug 2022]*
