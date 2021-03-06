_source: [KiCad Teensy E-Paper Badge](https://oshpark.com/shared_projects/1CiimZcf)_
## E-Paper Badge with Teensy LC designed in KiCad
E-Paper badge designed in [KiCad](http://kicad-pcb.org/) to connect [Pervasive Displays 2.15" E-Paper (E2215CS062)](http://www.digikey.com/product-detail/en/pervasive-displays/E2215CS062/E2215CS062-ND/5975949) to [Teensy LC](http://store.oshpark.com/products/teensy-lc). _([Teensy 3.2](https://oshpark.com/teensy) is also compatible)._  Based [Teensy E-Paper Shield](https://blog.oshpark.com/2016/08/27/teensy-e-paper-shield/) by [Jarek Lupinski](https://hackaday.io/Jarek) in EAGLE.

[![Photo of E-Paper Display](https://raw.githubusercontent.com/pdp7/kicad-teensy-epaper/master/images/small/epaper-badge-7.jpg)](https://oshpark.com/projects/1CiimZcf)

## KiCad PCB design files:
* repo: [kicad-teensy-epaper](https://github.com/pdp7/kicad-teensy-epaper/)
* commit: [Reworked layout for aesthetics [0a40263]](https://github.com/pdp7/kicad-teensy-epaper/commit/0a4026351685b28afe0d5b1825abe197254be2be)
* requires KiCad library [wickerlib](https://github.com/wickerbox/wickerlib) by [Jenner Hanni](http://jennerhanni.net/) of [Wickerbox Electronics](http://wickerbox.net/) for the 34-position FPC connector that the e-paper display plugs into:
  * [CONN-HEADER-FH34SRJ-34S-0.5SH.kicad_mod](https://github.com/wickerbox/wickerlib/blob/master/libraries/Wickerlib.pretty/CONN-HEADER-FH34SRJ-34S-0.5SH.kicad_mod)

## Bill of Materials (BoM)
### [Digi-Key shopping cart](http://www.digikey.com/short/3wbn09)
[![Digi-Key shopping cart](https://raw.githubusercontent.com/pdp7/kicad-teensy-epaper/master/images/small/kicad-epaper-digikey-bom.png)](https://raw.githubusercontent.com/pdp7/kicad-teensy-epaper/master/images/kicad-epaper-digikey-bom.png)
### Battery Power
* These products are used to power the badge from a battery.
* [LiPo battery charger add-on for Teensy 3.1](https://www.tindie.com/products/onehorse/lipo-battery-charger-add-on-for-teensy-31/) from Pesky Products on Tindie
     * WARNING: The trace between VIN and VUSB must be cut! Here is an [demostration of cutting the trace](https://learn.adafruit.com/assets/28069) on Adafruit Learning System.
* [Lithium Ion Polymer Battery - 3.7v 500mAh](https://www.adafruit.com/product/1578) from Adafruit
     * Initial capacity chosen for a good trade off between weight and power. I have not yet measured how long it will run with different capacities.

## Source Code
* uses [EPD215](https://github.com/jarek319/EPD215) Arduino Library by Jarek Lupinski for his E-paper Teensy Shield
* requires pinout modification:
  * [EpaperQuoteDisplay.ino](https://github.com/pdp7/kicad-teensy-epaper/blob/master/code/EpaperQuoteDisplay.ino)
  * `EPD215 epaper( 17, 16, 14, 15, 13, 11 );`

## Photos
* [Google Photos gallery](https://goo.gl/photos/csZV9jxah2BSP6vG9)
* [images directory in github repo](https://github.com/pdp7/kicad-teensy-epaper/tree/master/images)

## Video
* [YouTube: *E-Paper Badge with Teensy LC designed in KiCad*](https://www.youtube.com/watch?v=AxnLgPFTEOA)

## Related: Jarek's ePaper Teensy shield
  * OSH Park shared project: [Teensy e-Paper shield](https://oshpark.com/shared_projects/3KynIVn6)
  * My repo of Jarek's design files: [TeensyEpaperShield](https://github.com/pdp7/TeensyEpaperShield)
