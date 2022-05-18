# Improved Harbin Repairs Adapter PCBs

![photo of the adapter PCBs](img/v02_adapters.png)

This repo has modified versions of the
[Harbin Repairs](https://harbinrepairs.com/) adapter PCBs
for Haswell Optiplex systems (Optiplex 7020, Optiplex 9020,
Optiplex XE2, and Precision T1700.)

These PCBs allow Optiplex motherboards to be used in a standard
Micro-ATX case, which (in my opinion) is a very nice option for
building a useful PC from inexpensive and widely available components
salvaged from decommissioned Dell systems.

I modified the 5/6 pin power switch adapter and the 20 pin front-panel
USB2, audio, and HD LED adapter so that they would not hang off of the
edge of the motherboard. This allows them to be used in cases where
the motherboard is physically close to the edge of the case or
the power supply.

Examples of cases in which the original PCBs don't work:

* Rosewill LINE-M (power switch PCB doesn't fit because the
  power supply obstructs it)
* Compaq Presario SR2000 series (20 pin front-panel PCB doesn't
  fit because the bottom of the case obstructs it)

## Why I created a completely new repository

Originally I forked the Harbin Repairs repository, which is
here: <https://github.com/HarbinRepairs/Dell-Optiplex-MB-Header-Adapters>

However, I was not able to make changes to the KiCad project for
the 20 pin adapter PCB because the filenames are too long.
Also, when I tried to open the PCB design for the 20 pin adapter,
I could not see any traces, but the rats nest also showed that
there were no unconnected nets. I think this might have something
to do with an autorouter being used in the original PCB design.
In any case, I created an entirely new PCB design for this adapter,
based on the original schematic.

## Do they work?

Yes, they do work. I made a video in which I populate and test both
adapters: *link to video coming soon*

## Fabrication and construction

I used [OSHPark](https://oshpark.com/) to fabricate the PCBs. It is
incredibly simple: just upload the `kicad_pcb` files, then place your
order.

When you have the PCBs, you will need the following parts:

Part | Needed for | Note
---- | ---------- | ----
[0805 470 Ohm surface-mount resistor](https://www.digikey.com/en/products/detail/te-connectivity-passive-product/CRG0805F470R/2380909) | 20-pin adapter | Exact value is not critical
[2x10 2mm female header](https://www.digikey.com/en/products/detail/sullins-connector-solutions/NPPN102AFCN-RC/804795) | 20-pin adapter | connects to 2x10 male header on motherboard
2x5 2.54mm male header | 20-pin adapter | HD audio: remove second pin from bottom row
2x5 2.54mm male header | 20-pin adapter | USB2: remove first pin from top row
1x2 2.54mm male header | 20-pin adapter | HD LED
[2x3 2mm female header](https://www.digikey.com/en/products/detail/sullins-connector-solutions/NPPN032AFCN-RC/804788) | 5/6-pin adapter | connects to 5 pin header on motherboard
2x3 2.54mm male header | 5/6-pin adapter | power switch, power LED, diagnostic LED

I have linked to 2mm headers and a resistor on Digi-Key that I believe are correct.
However, I bought the 2x10 and 2x3 2mm female headers on Ebay, and I used a resistor
I already had on hand. It likely that any 2mm female headers you find will work.

The 2.54mm pin headers are just standard ones with square pins. You should be able
to find them just about anywhere.

## License

These modified PCBs are licensed under the GPL-3.0 license (the same
as the original PCBs.)

You can send feedback to me at <mailto:david.hovemeyer@gmail.com>.
