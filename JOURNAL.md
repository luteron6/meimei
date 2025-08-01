---
title: "meimei"
author: "@luteron6"
description: "A keyboard that's not too big and not too small"
created_at: "2025-06-20"
---
# meimei
Made by @luteron6

Total hours so far: 12

Estimated Cost: $150

I don't have a (regular) mechanical keyboard, and so I thought I'd build one for Hack Club's #highway YSWS.
Ok I've been thinking about this for a while, and here's what I want (some goals):
* 80%. I don't use all those extra keys, so 80% is great. I'm going to copy my existing laptop layout (kind of).
* A rotary encoder for volume control.
* Bluetooth with a battery
* USB-C
* Clicky keys :)

## Day 1 - 6/20/2025 - 7:55 AM (5 hours)
From my research, Cherry Blues are the typical 'clicky' switches. So I'll go with those. For the keycaps, I found [these](https://www.amazon.com/Japanese-Keycaps-Sublimation-Mechanical-Keyboard/dp/B08Y6S1N3X/).

I also found that the [nice!nano](https://nicekeyboards.com/nice-nano/) microcontroller is the typical bluetooth microcontroller used on keyboards. Apparently it's best on ZMK, so I'll have to learn that to make the firmware (I only know QMK). The docs also suggest socketing the nice!nano, so I'll try that. I found these sockets and pins: [here](https://ringerkeys.com/products/peel-a-way-sockets?variant=40212560576594).

Here's the start of my BOM:
* [Cherry Blue MX Keyswitches](https://www.amazon.com/Switches-Mechanical-Keyboard-Pre-Lubed-Pin-Enhanced/dp/B0CJ8SGL6B/): $32.99
* [Keycaps](https://www.amazon.com/Japanese-Keycaps-Sublimation-Mechanical-Keyboard/dp/B08Y6S1N3X/): $25.99
* [nice!nano](24.99) WOW! That's *expensive*: $24.99
* [Sockets/Pins](https://ringerkeys.com/products/peel-a-way-sockets?variant=40212560609362): $8.00
* [1N4148 Diodes](https://www.amazon.com/BOJACK-Switching-IN4148-Electronic-Silicon/dp/B07Q4F3Y5W/): $5.99

Here's the layout I want to go with:
![image](https://github.com/user-attachments/assets/0a6f3b77-ff0d-4b10-85b8-d3b4e23b0744)

I drew out my electrical matrix:<br>![Screenshot 2025-06-19 092204](https://github.com/user-attachments/assets/ee18e4a0-76f7-416f-8854-a1c9a4934743)

Then I created my schematic:<br> ![image](https://github.com/user-attachments/assets/4fb5aa7d-1b3c-4acd-a197-c92882329fbd)

Phew! It's done. My PCB, that is: <br> ![image](https://github.com/user-attachments/assets/bf424c90-40c9-4166-a9b3-6732c40d1c17)

I'm going to start on my case after I add this repo to the submissions.yml file. But I'm going to close this journal log now, it's been a while.


## Day 2 - 7/2/2025 last night (4 hours)
OK last night I stayed up way too late making my case. It was like past 11, so I just went to sleep without journaling. Anyway, I started and almost finished my case. Here's my PCB:

![image](https://github.com/user-attachments/assets/958eedb6-cede-423a-aad6-0bf660635a89)

I also decided to add a metal latching switch for turning the keyboard on and off, but the only downside is that it must be 'on' to charge. I also put a spot for the battery in there. I also added holes in the PCB so I can screw the plate into the bottom:

![image](https://github.com/user-attachments/assets/011a3a4f-1ded-4d32-a910-9bcb510503c3)

The whole case looks like this:
![image](https://github.com/user-attachments/assets/19bc7aa0-516d-4ce5-9ca0-17643d644717)
I think that's it for the case. Today (7/3) I'll try to work on the ZMK firmware.

## Day 3 - 7/3/2025 - 12:22 PM (3 hours)
I just spent way too long trying to figure that out. Hackatime says I spent around 2 hours trying to configure ZMK, then I probably spent another hour waiting for the workflow to run and troubleshooting the errors. But it did end up running, and [here](https://github.com/luteron6/zmk-config-meimei/actions/runs/16058502554e) are the results.

I think it's almost ready to submit!

## Day 4 - 7/27/2025 - 7:58 AM (1 hour)
Yesterday I purchased all the parts for the keyboard. I could only find some parts on certain sites, so I got those first. The rest was from Amazon. I was looking to source from Aliexpress, but stuff wasn't looking much cheaper there. So most of it's coming from Amazon.

