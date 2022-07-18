# Updates
All notable updates to this project will be documented in this file.

*(The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).)*

> [PCBWay](https://pcbway.com) graciously offered to sponsor the prototype build of this keyboard

<p align="center">
<a href="https://pcbway.com/"><img src="../pcbway.jpg"></a>
</p>

## Up Next

- [ ] Solder on LED's, Hot-Swap sockets
- [ ] More PCB Testing - LED
- [ ] QMK code finalization
  - [ ] VIA support & test EEPROM

---

# History

## 2022-06-17

- Order placed with PCBWay and confirmation received.


## 2022-06-28

### Finished goods photos sent

- Got an email will the finished build - shipping to me next.
  
  <a href="prod_1.jpg"><img src="prod_1.jpg" width="10%"></a>
  <a href="prod_2.jpg"><img src="prod_2.jpg" width="10%"></a>
  <a href="prod_3.jpg"><img src="prod_3.jpg" width="10%"></a>
  <a href="prod_4.jpg"><img src="prod_4.jpg" width="10%"></a>
  <a href="prod_5.jpg"><img src="prod_5.jpg" width="10%"></a>


## 2022-07-15

### PCB delivered

- Arrived in Sydney via DHL.  No issues.


## 2022-07-18

### Initial testing

- Soldered on UBS connector
- Soldered on MicroMod connector
- Insyalled SMT32 module and Tested key matrix - ***IT WORKS!***
  - must say I build 2 boards and both didn't work at first - fault finding lead to discovery that one of the USB data lines was grounded.  On one board I stripped out the ESD thinking that was up-side-down... it wasn't.  And then I found it.  A solder short on the MicroMod connector between pin 5 and 7... on BOTH!
  - Next time I will have all the components installed by the supplier!
- PCBWay did an amazing job on the PCB!


---

# Issues
> as discovered ... to implement in rev. B

- [ ] Position of MicroMod connector is too low, does not fit in AP2 case without minor cutting - possibly move this up as far as it can go.
- [ ] Position of the BOOT pads in the space bar area should align to the AP2 slot

## Maybe

- [ ] Possibly Move 5678 LED's to north-facing.
- [ ] Possibly incorporate a ISO layout?
- [ ] Possibly incorporate a 64-key layout?
