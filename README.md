# Improved Harbin Repairs Adapter PCBs

This repo has modified versions of the Harbin Repairs adapter PCBs
for Haswell Optiplex systems (Optiplex 7020, Optiplex 9020,
Optiplex XE2, and Precision T1700.)

These PCBs allow Optiplex motherboards to be used in a standard
Micro-ATX case, which (in my opinion) is a very nice option for
building a useful PC from inexpensive and widely available components
salvaged from decommissioned Dell systems.

I modified the 5-6 power switch adapter and the 20 pin front-panel
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

## License

These modified PCBs are licensed under the GPL-3.0 license (the same
as the original PCBs.)

You can send feedback to me at <mailto:david.hovemeyer@gmail.com>.