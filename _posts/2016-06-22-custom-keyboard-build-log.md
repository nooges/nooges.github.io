---
layout: single
title: Custom keyboard build log
tags: []
modified: 
comments: false
author_profile: true
---

Within the past couple of months, I've started to get into using mechanical keyboards. I don't exactly know what spurred me to try them out, but now I'm hooked, and it's hard to avoid going to [/r/mechanicalkeyboards](https://reddit.com/r/mechanicalkeyboards). After hanging out there for a while and seeing people do custom keyboard builds, I decided to do my own build. So here's a log of my build (currently in progress, as I wait for all the parts to arrive).

## Keyboard Type
One of the builds I saw on Reddit was of a [5x13 ortholinear keyboard](https://www.reddit.com/r/MechanicalKeyboards/comments/4m2cbg/photos_custom_5x13_keyboard/). It looked pretty cool, and the maker posted up the file for the case design, so I decided to go with that, as opposed to designing something from scratch.

## Parts and Costs
Here's a breakdown of parts and costs:

| **Item** | **Price** | **Source** | **Notes** |
| Switches | $19 | [SwitchTop](http://www.switchtop.co/product/gateron-switches) | 63 Gateron Brown switches |
| Case | $18.50 | [Ponoko](https://www.ponoko.com/) | 3mm clear acrylic case |
| Diodes | $0.60 | [eBay](https://ebay.com) | 63 1N4148 diodes (bought a pack of 500) |
| Pro Micro Controller | $4.09 | [AliExpress](http://www.aliexpress.com/item/Mini-Leonardo-Pro-Micro-ATmega32U4-5V-16MHz-Module-For-Arduino-Best-Quality/32284746884.html) | |
| Standoffs/Screws | $1 | [eBay](https://ebay.com) | Bought an assortment set of M2 screws/standoffs |
| Keycaps | $13.50 | [/r/mechmarket](https://reddit.com/r/mechmarket) | Bought a pack of about 70 random DSA keycaps |
| Wires | $0 | Home lab | Already have a bunch of 22 AWG wire hanging around in my home lab (a.k.a garage) |

## Case
The case is made of 5 layers of 3mm acrylic. I simply took the design posted on Reddit and sent that off to Ponoko for cutting. The design was for Ponoko's P2 size acrylic sheets, and I went with a clear sheet. For first time Ponoko customers, there's $20 off the first project, which is pretty sweet.

Here's the different layers, after I popped them off of the big sheet that came in the mail. Note that I hadn't peeled off the paper backing on the acrylic yet to protect them from being scratched.

![img_3834](https://cloud.githubusercontent.com/assets/204212/16386576/235a9d34-3c5f-11e6-9256-15e44f33ca42.JPG)

![img_3952](https://cloud.githubusercontent.com/assets/204212/16386574/2355ac52-3c5f-11e6-9f7c-b07d053f077e.JPG)

## Installing the switches
Normally, the switches are used with 1.5mm thick plates, where they snap in just fine. Because the acrylic is 3mm thick to prevent the keyboard from flexing too much, the switches don't snap in place when inserted. So I had to glue all the switches in place to prevent them from being pulled off while removing a keycap.

For the spacebar, I went with a 2u wide spacebar and needed to install stabilizers for it. I got Cherry stabilizers, but had to file off parts of it to get it to fit on the plate. Unfortunately, I cracked part of the acrylic while trying to figure out how to install one of the stabilizers.

Back side of the plate
![img_3953](https://cloud.githubusercontent.com/assets/204212/16386573/2355833a-3c5f-11e6-8b1b-88c9a0cddcf5.JPG)

Front side of the plate
![img_3954](https://cloud.githubusercontent.com/assets/204212/16386575/2355a9e6-3c5f-11e6-8fe5-3aae82f1e0d9.JPG)

Another shot of the back side, you can see where I cracked the plate next to the right stabilizer
![img_3955](https://cloud.githubusercontent.com/assets/204212/16386572/235568f0-3c5f-11e6-9778-4d1ef39ea877.JPG)

## Keycaps
I've been eyeing DSA keycaps for a while, and I happened to be browsing [/r/mechmarket](https://reddit.com/r/mechmarket) at just the right time, when someone posted DSA caps for a good price. Seems like those go fast these days. The set I got only came with some of the keys for the number row, and everything else is just random. I don't particularly care for what legends are on there, as it's not like I look at the keyboard to type.

Still need to buy a 2u DSA keycap for the spacebar here:
![img_3999](https://cloud.githubusercontent.com/assets/204212/16386571/235471a2-3c5f-11e6-94bb-cd4847335e42.JPG)

## Busting out the soldering iron (still in progress)
Still awaiting for the diodes to arrive before moving on to handwiring the board.

## Programming the keyboard layout (still in progress)
I've figured out where I want most of the keys already for the main layer, still trying to feel out where I want to put the various modifier keys. I also still need to figure out what keys to place on the other layers. Here's my work in progress [layout](http://www.keyboard-layout-editor.com/#/gists/e3fc42ca0945b077596cbb2d0399d05d).
