---
layout: single
title: Custom 5x13 keyboard build log
tags: []
modified: 2016-11-08
comments: false
author_profile: true
---

Within the past couple of months, I've started to get into using mechanical keyboards. I don't exactly know what spurred me to try them out, but now I'm hooked, and it's hard to avoid going to [/r/mechanicalkeyboards](https://reddit.com/r/mechanicalkeyboards). After hanging out there for a while and seeing people do custom keyboard builds, I decided to do my own build. So here's a log of my build.

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
| Keycaps |  | [/r/mechmarket](https://reddit.com/r/mechmarket) and [PMK](https://pimpmykeyboard.com) | [PMK grab bag](http://pimpmykeyboard.com/grab-bags/) and trades |
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

Originally, I was going to use DSA keycaps and bought some random ones from someone off of [/r/mechmarket](https://reddit.com/r/mechmarket):
![img_3999](https://cloud.githubusercontent.com/assets/204212/16386571/235471a2-3c5f-11e6-94bb-cd4847335e42.JPG)

But while waiting for other parts to arrive, I bought [2 grab bags from PMK](http://pimpmykeyboard.com/grab-bags/) and ended up liking the SA profile keycaps a lot more. I got a ton of [PuLSE SA](https://www.massdrop.com/buy/pulse-sa-keycap-set?mode=guest_open) and trading with others to get a more complete set.

## Busting out the soldering iron
I had to wait a while for the diodes to arrive before moving on to handwiring the board, since I ordered them from eBay and they were shipped from China. For each of the diodes, I took a pair of pliers and bent it at a sharp 90 degree bend. Some people take a bunch of diodes and bend them all at once, but using the pliers gives a much neater look in my opinion.

To wire up the columns, I use [22 AWG hookup wire](https://www.amazon.com/Elenco-Hook-Up-Colors-dispenser-WK-106/dp/B008L3QJAS/) that comes in a pack of 6 colors:
![Hookup Wire](https://images-na.ssl-images-amazon.com/images/I/81NPHtQS%2BkL._SL1500_.jpg)

For each column, I cut a length of wire to go from the top row to the bottom and then used a wire stripper to remove some of the insulation. Here's the board after adding the first column wire:
![First column](http://i.imgur.com/eucjOdG.jpg?1)

After adding all the column wires, I soldered the diodes to the switches and to each other. Having one of those helping hands tools helps out immensely here. Here's how it looked after doing the first row:

![First row](http://i.imgur.com/WwMISl0.jpg)

All rows complete:

![All rows done](http://i.imgur.com/3ck7RuQ.jpg)

## Adding the microcontroller

The microcontroller for the keyboard is a Pro Micro, which has a Micro USB port on it. I first soldered wires onto the microcontroller before connecting them to the keyboard.

![Soldering wires to the Pro Micro](http://i.imgur.com/hCYjUsp.jpg)

![All wires on Pro Micro](http://i.imgur.com/i79m0i9.jpg)

It's easier to make the wires longer than needed, so you can move the microcontroller around a bit to figure out the best place for it.

![Microcontroller installed](http://i.imgur.com/HEMlIbW.jpg)

### USB adapter and reset switch

Next, I created a Micro USB to Mini USB adapter. I took a Micro USB cable, shaved off all of the insulation on it and soldered it to a female Mini USB receptacle I had (free sample from Molex acquired many years ago). I hot glued the Mini USB receptacle to cutout in the case. I also added a reset switch for the microcontroller, which is needed for reflashing it with new firmware. Kind of a crap ass job with the yellow electrical tape here, but whatever, it works.

![USB and reset switch](http://i.imgur.com/NLNixQa.jpg)

Before closing up the case, I added some memory foam to help dampen noise from the switches and to prevent the top layer of the keyboard from flexing. I got a free sample of memory foam from [Tempur-Pedic](https://register.tempurpedic.com/tempurme/)

![Closed bottom and foam](http://i.imgur.com/ze9kZFz.jpg)

## Programming the keyboard layout
I've figured out where I want most of the keys already for the main layer, still trying to feel out where I want to put the various modifier keys. I also still need to figure out what keys to place on the other layers. Here's my work in progress [layout](http://www.keyboard-layout-editor.com/#/gists/e3fc42ca0945b077596cbb2d0399d05d).

For the firmware, I used the [QMK firmware](https://github.com/jackhumbert/qmk_firmware), which was not too hard to setup. I created my [own fork](https://github.com/nooges/qmk_firmware/tree/preonix) to add in a 5x13 layout since there wasn't one in there. The tricky part was trying to figure out how to flash the Pro Micro, as the firmware is mainly setup to flash the Teensy 2.0 microcontroller. I had to convert the pinouts to the Pro Micro and use AVRDUDE to flash it.

## Result

Here's the final result!

![Final keyboard](http://i.imgur.com/8DD7dEW.jpg)

After putting everything together and using the keyboard, turns out there's a couple of things that annoy me about it. First, the combination of SA keycaps and stock brown switches makes the keys too easy to press. Second, I've now realized that I prefer my spacebar to just be a 1u key, instead of a 2u key, since I only hit the spacebar with my left thumb.

I'll swap out the stock Gateron brown springs with heavier ones at some point, but that's going to be a bit of a pain, because despite having the top layer cut with switch slots that allow the switch top to be removed, the way I hot glued the switches prevents the top from being removed. I'll have to remove all the glue on the left and right sides of the switches.

As for the ortholinear layout of the keys, as opposed to the normal staggered layout you normally see, it did take some getting used to the bottom row of letters. There is a bit of an adjustment phase to press the C, V, B, N, and M keys correctly, which seems to be a common problem from what I heard, but it took me about a week to get used to it. I regularly switch between ortholinear and staggered layout keyboards, and I haven't had a problem going back and forth.
