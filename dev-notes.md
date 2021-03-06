# Random Notes

***(Not part of the project)***

## MicroMod reference boards

- SparkFun MicroMod ATP Carrier Board - https://github.com/sparkfun/MicroMod_ATP_Carrier_Board
- SparkFun STM32 MicroMod Processor - https://github.com/sparkfun/MicroMod_STM32_Processor
- SparkFun MicroMod Processor RP2040 - https://github.com/sparkfun/MicroMod_Processor-RP2040

## Tools Used

- Layout
    - [Keyboard Layout Editor](http://www.keyboard-layout-editor.com/)
- EAGLE key position generator
    - [Kalerator](https://kalerator.clueboard.co/)
- KiCad
    - [@ai03 's PCB Designer Guide](https://wiki.ai03.com/books/pcb-design/chapter/pcb-designer-guide)
    - [@ruiqimao 's Keyboard PCB Guide](https://github.com/ruiqimao/keyboard-pcb-guide)
- Plate
    - [Swill's Plate & Case Builder](http://builder.swillkb.com/)
    - [Keyboard CAD Assistant](http://www.keyboardcad.com/)


## Possible design aids

- Closest is the BM60 Poker - but that's not open source.
- [**Acheron Project**](https://github.com/orgs/AcheronProject) - [acheronproject.com](https://acheronproject.com/)
    - [KeebsPCB](https://github.com/AcheronProject/KeebsPCB) &#x26A0;
    - [ArcticPCB](https://github.com/AcheronProject/ArcticPCB)
    - [Tsuki](https://github.com/AcheronProject/Tsuki)
    - [Doddle60](https://github.com/AcheronProject/Doddle60)
- [GH60](https://github.com/komar007/gh60), also [read this](http://blog.komar.be/gh60-evolution/)
- [Bakeneko 60](https://github.com/kkatano/bakeneko-60)
- [Voyager 60](https://github.com/ai03-2725/Voyager60)
- [Plain6-C](https://github.com/evyd13/plain60-c)
- *(a bit off the design footprint)* [Grabert KB](https://github.com/KoBussLLC/grabert-hardware)
- for M.2 example see [github.com/makerdiary/python-keyboard](https://github.com/makerdiary/python-keyboard) & [makerdiary.com/m60](https://makerdiary.com/pages/m60-mechanical-keyboard)

## @tzarc Notes

Explicitly listed below, pins are available on all of:
> STM32, SAMD51, Teensy, RP2040, nRF52

- A0/A1 available
- PWM0/PWM1 available
- D0/D1 available
- G0-G3 available
- AUD LRCLK/BCLK available
- I2C SCL/SDA/INT available
- SPI SCK/SDO/SDI/CS available

further:

- G4-G7 are unusable on RP2040 (collides with SPI)
- CAN only available on STM32, SAMD51, Teensy
- G11/SWO only available on STM32, SAMD51, Teensy