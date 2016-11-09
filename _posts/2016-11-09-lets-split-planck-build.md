---
layout: single
title: Let's Split - Split Planck Keyboard Build
tags: [keyboard]
modified: 
comments: false
author_profile: true
thumbnail: http://i.imgur.com/TYsH3F9.jpg
---

## A Board I Didn't Need

One day, I was slacking off by browsing [/r/mk](https://reddit.com/r/mechanicalkeyboards) as usual, when someone posted up a group buy on split Planck (a.k.a Let's Split) PCBs for $6 a pair. I wasn't really that interested in having a Planck, but for $6, I figured, "What the heck, why not?"

![Empty board](http://i.imgur.com/VcqOQfD.jpg)

After receiving the boards, they just sat around for a while, since I still hadn't finished my [other keyboard build](/custom-keyboard-build-log). Even after finishing that, I needed to order some more switches and get some acrylic plates cut.

## Plates

As usual, I put together a design to be sent off to Ponoko for cutting. Instead of just getting the parts cut for the split Planck alone, I figured I might as well have a couple of other keyboard layouts cut. On the left side of the plate, is the split Planck pieces, the top right is an [Atreus](https://atreus.technomancy.us/) modified to have an extra column on each half, and the bottom right piece is the bottom plate for a regular Planck (already bought a stainless steel plate from [OLKB](http://olkb.com/planck/top-plate)).

![Full Ponoko plate](http://i.imgur.com/FfGWHOt.jpg)

A closer view of the plates. During the layout editing process, I must've done a bad copy and paste job at some point, because some of the holes are in the wrong place. You might notice that the holes on the left plate are slightly shifted to the left. The mounting holes on the bottom plate for the Planck are way off to the left and one of the holes overlapped with one of the Atreus holes. I need to be a bit more careful next time around.

![Closer view](http://i.imgur.com/3tbI3Sd.jpg)

## It's Solderin' Time

First, I started off by soldering on the diodes.

![Diodes](http://i.imgur.com/N8xH0dl.jpg)

Next came the header pins for the Pro Micro. After I solder the header pins on, I pried off the plastic that grouped them together so the microcontroller could be more flush with the PCB.

![Header pins](http://i.imgur.com/XMqwtiv.jpg)

After that, I soldered on the 3.5mm TRRS jack, followed by Gateron brown switches. Then, I added on the Pro Micro and clipped the excess header pins. I also soldered a reset switch directly to the Pro Micro, but after I took this picture and tested out the bottom plate, I realized that I had to flip the switch upside down.

![Pro Micro and reset switch](http://i.imgur.com/o95dhyD.jpg)

Corrected orientation of the reset switch, much better now. To hit the switch, I take a tiny flat-head screwdriver to press it.

![Flipped reset switch](http://i.imgur.com/nfeUCpe.jpg)

## Final Steps

### Spring swap

After my bad experience with brown switches and SA caps on my previous build, I swapped out all the stock springs in the switch with [67g ones from Switchtop](http://www.switchtop.com/product/custom-cherry-mx-switch-springs). I should probably try out MX Clears at some point, but this will do for now. The [switch top removal tool](https://mechanicalkeyboards.com/shop/index.php?l=product_detail&p=1363) was purchased from [MechanicalKeyboards.com](https://mechanicalkeyboards.com).

![Spring swap](http://i.imgur.com/kaVPlPO.jpg)

### Programming the board

Each half of the keyboard has their own Pro Micro controller and talks to each other over the TRRS cable. Both halves were flashed with the [Let's Split portion of the QMK firmware](https://github.com/jackhumbert/qmk_firmware/tree/master/keyboards/lets_split). I added a couple of [my own modifications](http://www.keyboard-layout-editor.com/#/gists/fbabb2e372ff4d349257afde1a81f7be) to the base layout, mainly to place Backspace on the right thumb and backtick/tilde in the lower left corner.

![Layout](http://i.imgur.com/XIr6Dss.png)

### Final result

![Final](http://i.imgur.com/TYsH3F9.jpg)
