# meimei
A simple, wireless, 75% keyboard! Not too big or small. It runs ZMK.

![image](https://github.com/user-attachments/assets/19bc7aa0-516d-4ce5-9ca0-17643d644717)


# Why?
My first exposure to keyboards was through Hack Club's #hackpad, in which I made a 5-key macropad with an encoder and screen. I've never had a regular mechanical keyboard, and this is my attempt at making one. It has a function row, all the necessary keys for typing, and a rotary encoder. Since I mainly use a laptop, I wanted this keyboard to be fully wireless.

## Code - ZMK
After watching many [Joe Scotto](https://www.youtube.com/@joe_scotto) videos, I came to the conclusion that the only reasonable microcontroller to use was the [nice!nano v2](https://nicekeyboards.com/docs/nice-nano/pinout-schematic).

It's suggested to run ZMK as the firmware for bluetooth, so I learned ZMK for this keyboard. Previously I've used QMK, but ZMK is quite different as it uses a Github Actions workflow to compile the firmware file. The firmware for this keyboard lives in [this](https://github.com/luteron6/zmk-config-meimei) repository. Simply go to the [Actions](https://github.com/luteron6/zmk-config-meimei/actions) tab, open the most recent workflow, download the firmware Artifact, unzip the firmware, and flash it to the nice!nano. 

All the source files for ZMK are in the /Code folder in this repository.

## PCB
I made the PCB in KiCad, using [Joe Scotto's symbol/footprint/3D model library](https://github.com/joe-scotto/scottokeebs/tree/main/Extras/ScottoKicad).

It was really helpful as his footprints had 3D models linked to them, because it transferred into Onshape when I worked on my CAD. I included a power button to turn off the keyboard when I travel with it, and an encoder for good measure.

I chose to go with the biggest reasonable battery for this project, so I chose a 3048128 3400mAh battery. According to the [ZMK Power Profiler](https://zmk.dev/power-profiler), this keyboard will last 1 year and 1 month. So basically forever. And ZMK can report battery usage over bluetooth, so this keyboard will literally never die.

The PCB files are in the /PCB folder, including the KiCad source files and the Gerbers for production.

![image](https://github.com/user-attachments/assets/bf424c90-40c9-4166-a9b3-6732c40d1c17)


## CAD
As mentioned above, the CAD was made in Onshape. The case has two parts, both of which are in the /CAD folder along with the STEP file of everything. It's meant to be 3D printed and screwed together using threaded inserts and M2 screws.


## BOM
| Item                     | QTY Needed | QTY Purchased | Price   | Description          | Link                                                                                             |
|--------------------------|------------|----|---------|---------------------------------|--------------------------------------------------------------------------------------------------|
| Keyswitches              | 74         | 90 | $27.98  | Clicky switches                 | [Link](https://www.amazon.com/Akko-Keyboard-Diffuser-Mechanical-Structure/dp/B0DJNSK6TD/)        |
| Keycaps (Japanese Maple) |            |    | $25.99  |                                 | [Link](https://www.amazon.com/Japanese-Keycaps-Sublimation-Mechanical-Keyboard/dp/B08Y6S1N3X/)   |
| nice!nano                | 1          | 1  | $24.99  | microcontroller                 | [Link](https://www.littlekeyboards.com/products/nice-nano)                                       |
| PCB                      | 1          | 5  | $30.00  | JLCPCB (also includes shipping) |                                                                                                  |
| diodes                   | 70         | 125 | $5.99  | SOD-123 package diodes          | [Link](https://www.amazon.com/100-Pieces-1N4148W-Switching-High-Speed/dp/B079KJX5J9/)            |
| Stabilizers              |            |    | $18.99  | Spacebar/2u stabilizers         | [Link](https://www.amazon.com/DUROCK-Stabilizers-Translucent-Keyboard-Mechanical/dp/B0B2RVN19F/) |
| peel-away sockets        | 2          | 2  | $6.00   | socketing the microcontroller   | [Link](https://ringerkeys.com/products/peel-a-way-sockets?variant=40212560576594)                |
| peel-away pins           | 2          | 2  | $6.00   | socketing the microcontroller   | [Link](https://ringerkeys.com/products/peel-a-way-sockets?variant=40212560609362)                |
| Battery                  | 1          | 1  | $8.99   | A 3048128 3400mAh battery       | [Link](https://www.amazon.com/YTKavq-3400mAh-Battery-Rechargeable-Connector/dp/B08TTJ79JV/)      |
| Latching Switches        | 1          | 3  | $7.99   | Power on/off switch             | [Link](https://www.amazon.com/Gebildet-Prewired-Waterproof-Self-Locking-Stainless/dp/B0BXPFW69R/) |
| littlekeyboards shipping |            |    | $6.00   |                                 |                                                                                                   |
| ringerkeys shipping      |            |    | $6.00   |                                 |                                                                                                   |
| Total                    |            |    | $174.92 |                                 |                                                                                                   |