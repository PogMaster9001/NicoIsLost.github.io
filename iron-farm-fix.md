---
layout: page
title: 1.20.2 Iron Farm Fix
subtitle: Converting the NIL 1.19 Iron Farm to 1.20.2
latex: true
---
The 1.20.2 Update fixed a [bug that nerfed iron farms in 1.19-1.20.1](https://bugs.mojang.com/browse/MC-254100). The minimum time between golems in 1.19-1.20.1 was 700 game ticks, but in 1.20.2 the minimum time between golems is 600 games ticks, which moves it back to the 1.14.3 - 1.18.4 mechanics.

As such, farms that were designed for 1.19 mechanics need to be modified -- Like the 1.19 version of the Nico is Lost Stackable Iron Farm.

# 1.19 Farm Fix
![1.20.2 Iron Farm Fix](\assets\img\iron-farm-fix\fix.png)

The 1.19 version has 18 repeaters, (17) set to 4 ticks and (1) set to 2 ticks. The 1.20.2 version gets rids of 8 repeaters, for a total of 15 repeaters all set to 4 ticks.

This is to modify a pre-built farm. New farms should always be built in the 1.18 version. You can of course use any arrangement of repeaters, the goal is to get 60 game ticks for the repeater clock, since there are 5 hoppers in the counter, so 5 * 60 is 300 redstone ticks * 2 = 600 game ticks. 

Join the [discord](https://discord.nicoislost.com) if you need more help!