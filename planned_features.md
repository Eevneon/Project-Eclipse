## Lunar cycles
The lunar cycles have been a feature in minecraft for, ages, I'm pretty sure. The idea is simple: Some nights, you'll die. Some nights, you'll wonder why it's so quiet outside.
But personally? I don't think anyone really notices these cycles, let alone appreciate them. 

From now on, lunar cycles will work a bit different. They still cycle through eight variants, on and on and on forever, but every biome will react to these changes differently. 
For example, the most average biomes like plains, meadows, rivers, etcetera, will be on their easiest variant on the first night. This is to make sure that the first night is still a cohesive experience, like it's always been. 
However, this doesn't mean the first night is easy. As you might know, in vanilla minecraft, the first moon phase is the hardest one. But I don't hope I'm the only one to realize that the first night is not that hard. I think it's perfectly hard enough. But as you progress through the game, your equipment becomes better. Therefor,e I think it's weird that the mob spawning only becomes easier during the first 8 ingame days of your minecraft world.
So. Moderate biomes start out easy. They become harder. This means that either more mobs will spawn, or they will spawn with stronger equipment. With the newly added zombie horsemen, there are quite a few things to watch out for, considering this mod will boost jockey and horsemen spawns by quite a bit during harder moon phases.

Summarized, there are three variables that change during the lunar cycle:
- Density, or the amount of mobs that actually spawn during nighttime.
- Advancement, which regulates the level of equipment that mobs carry during nighttime.
- Entropy, which might be an odd term for this, but it regulates the diversity of mobs that spawn. Higher values also boost the amount of jockeys and horsemen that spawn at night.

### So, how do these variables work?
Well, to get into the math that will be used behind the scenes of this mod, all these variables will follow the absolute value of a sinusoid function, where every half period of the function will be equal to the length of a lunar cycle: eight days.
This way, every variable slowly climbs up to their max value, which will be roughly around the fourth or fifth day, only to decline later on.

Here's an extended explanation for all three variables:

Lets start with the most complicated one. **Entropy**, like mentioned before regulates the diversity of mobs that spawn. This is how that works:
This mod assigns a number (commonness or c-value) to every single type of mob, which is different for every biome. For example, husks, in deserts, will have a high c-value. This means it spawns a lot in deserts, no matter the phase of the moon.
However, endermen will have a lower c-value in deserts, so that it doesn't spawn as often. Then, as the lunar cycle progresses, and the entropy value reaches its maximum, you might see less husks. Most strong mobs will have the lowest c-values in most biomes, this way, when the entropy does actually increase, the game gets harder.
