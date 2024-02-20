---
layout: page
title: The Mob Spawning Algorithm
subtitle: Concepts and Equations
latex: true
---
The mob spawning algorithm is a very complex topic, but is also important to understand as a huge number of different Minecraft farms use natural mob spawning to function, and design and optimization of these farms requires an understanding of at least the basics of the mob spawning algorithm. 

# What is a "Naturally Spawned Mob"

The mob spawning algorithm is the function in the game that "naturally spawns" mobs. There are different ways in which mobs can show up in the same, sometimes they are generated with structures or biomes (villagers, vindicators), or they can be force spawned (think a warden, wither, & iron golems), and sometimes there are special spawning rules like pigmen spawning in portals and zombie reinforcements. 

These all use different dynamics than the mob spawning algorithm. Mobs that are "naturally spawned" show up seemingly random as you play the game -- most often in the dark parts of the world due to their spawning requirements. 

# The Mob Spawning Algorithm

In principle the mob spawning algorithm is a set of rules and checks that the game does before spawning a mob. The outcome of the algorithm is a regular distribution of these mobs according to the rules. There are three main phases of the algorithm: 

- The Mob Cap
- "The Bulk of the Algorithm"
- Despawning

In my mind the mob cap and despawning portions are auxiliary portions of the algorithm rather than part of the algorithm itself -- but that doesn't mean they aren't important! They are hugely impactful, but just a little bit less complicated. 

## The Basic Rules

Spawning works in spheres around players, there are a number of rules that govern where mobs spawn and despawn. 

- < 24 Blocks from a player: Mobs will not spawn
- < 32 Blocks from a play: Mobs don't despawn
- > 32 < 128 blocks from a player, after 30 seconds in this range: Mobs have a 1/800 chance of despawning every gametick.
- > 128 blocks from a player: Mobs instantly despawn

Note:
```Certain conditions will prevent the mobs from despawning, like if they picked up a player dropped item, if they are riding a minecart or boat, or have been nametagged. These also remove mobs from the mobcap, as we will discuss later.```

