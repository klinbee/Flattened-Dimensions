# Flattened Dimensions

### Tired of the boring single-biome vanilla superflat options?

Try out my Datapacks!
All of the datapacks in this collection let you generate Superflat-style worlds, but have **all the biomes and structures**.  
**Even including the Nether and the End dimensions!**

---

# Datapack Versions

## Superflat Dimensions

Modeled after the Classic Default Superflat preset.  
Boring to look at, an interesting challenge to play.  
[More images and download page](https://github.com/Klinbee/Better-Superflat-Datapacks/releases/tag/V1MC1.20)  
![image](https://github.com/Klinbee/Better-Superflat-Datapacks/assets/105707614/aae4e032-2fba-4e81-8119-73131e2e13ac)

## Superflat Dimensions II

Modeled after the Classic Default Superflat preset.  
Adds foliage[^1] and water to the Superflat Dimensions datapack. More aesthetically pleasing.  
[More images and download page](https://github.com/Klinbee/Better-Superflat-Datapacks/releases/tag/V2MC1.20)  
![image](https://github.com/Klinbee/Better-Superflat-Datapacks/assets/105707614/7ec717c7-0a71-4ae5-85d5-7b68ba91cbc5)

## Flat Dimensions

Modeled after the "Overworld" Superflat Preset  
All the land is capped at sea-level. Foliage,[^1] ores, rivers, and oceans all generate like normal.  
There is also another version of this that generates with caves.  
[More mages and download page](https://github.com/Klinbee/Better-Superflat-Datapacks/releases/tag/V3MC1.20)  
![image](https://github.com/Klinbee/Better-Superflat-Datapacks/assets/105707614/b7c5dab9-1970-43f0-95d4-8d2b1ba4e755)

---

### Some parts helped made with Jochen Jacobs' Snowcapped Tool!

[Snowcapped Multi-Noise Biome Tool Editor](https://snowcapped.jacobsjo.eu)  
[Jochen Jacobs' Github](https://github.com/jacobsjo)

---

### If you have any suggested changes to this, I can upload them for you (like adding a nether roof, redesigning the end, only overworld/nether/end superflat packs, etc.)

---

# FAQ

| Question                                                    |                                                                           Answer                                                                            |
| ----------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------: |
| "Why does X structure spawn in bedrock/below bedrock?"      |                                                           **It is unchangable using a Datapack**                                                            |
| "Will I die/can I build under the bedrock?"                 |                                          **You won't die, and you can build! The true bottom is still at y=-64.**                                           |
| "Why is the world at y=64?"                                 |                                             **Some structures won't spawn below that y-level, like Mansions.**                                              |
| "Why don't geodes/spawners spawn in the Classic Superflat?" |                                                 **There is sadly not enough terrain for them to generate.**                                                 |
| "Why does the End not generate as a perfect flat plane?"    | **End cities generate at y=64, the End Spawn Platform generates at y=50. Datapacks can't change this, so either no End Cities or spawn below the bedrock.** |
| "Are All Advancements possible on these?"                   |             **Yes! You should try to get them all ;). It can be quite the challenge on Superflat Classic, but the other versions are easier.**              |

# Technical Details of the Datapack

### About the Classic Superflat Versions:

- Mansions, Monuments, Strongholds, Mineshafts, End Cities and Nether Fossils[^2], all have hard-coded heights of generation, so they cannot be moved with a Datapack.
  - This is why the Superflat world generates at the height that it does. If were much lower, Mansions wouldn't generate.
  - This is also why Monuments cut through the bedrock, Strongholds and Mineshafts are under the bedrock. This presents an interesting challenge to the player, and is kind of funny.
    - Don't worry though! The true bottom of the world is at y =-64, so you can safely live, place blocks, and mine under the bedrock!
- On a similar note, Buried Treasures are hard-coded to generate a certain distance down (kind of? it's confusing) and won't generate naturally. I've solved this by recreating it as a custom structure, which has customizable heights.
  - Because of a quirk with custom structures, Buried Treasures won't generate at the (9,9) chunk coordinate (like they normally do, if you didn't know) and instead will generate at the (0,0) chunk coordinate.
  - Unfortunately it is very difficult to do this for the other structures mentioned above or I would do this.
- Technically, two types of foliage do generate in the "Classic Flat" preset, which are Kelp and Chorus Fruit (technically there are other End Features kept as well).
  - The significance of this is that the Advancement "A Balanced Diet" requires eating all food items. There is no other source of Chorus Fruit, and the only other source of Kelp is the Wandering Trader, which would be cumbersome.
  - With that, All Advancements are possible given the limitations. I've put the challenge up to you to figure out how ;). Some Advancements are straight-forward, and some convoluted.
- The main reason I made the Nether generate at y = 32 was to avoid the ugly void fog at the bottom of the Nether, and also to make it in-line with the overworld/end (as they generate at y = 64, felt right to go half that).
  - Additionally, that meant that Nether Ruined Portals wouldn't float (Again, unable to change height of generation).
- All of the structures that generate with a "beardifier" (function that adds generates terrain below a structure) made a big mess under the bedrock, so I removed that from all of those structures.
- One of the structures that can have it's height of generation changed is the Bastion, which I moved up slightly for the Nether.
- For some reason, stopping flowers from generating also stops them from being generated with bonemeal, even though this isn't true in the nether...

### About Version 3:

- Due to the strange world-height flattening, I've partially edited the Biome Parameters to make some of the underground biomes (specifically the deep dark) generate close to how it normally would.
- It seems that Desert Temple's and Jungle Temple's generation is linked to sea-level. I had to make identical custom structures in order for them to generate.
- Nether Fossils are the same way, which is strange. I tried the custom structure approach with them, but it didn't work properly because they would generate in lava and stick out.

[^1]: Foliage means the grass, trees, plants, and flowers that would normally generate in a world. In Minecraft though, these are called "features" and also include lava pools, spawners, geodes, fire patches in the nether, etc.
[^2]: Nether Fossils are for some reason are considered a structure in the code.
