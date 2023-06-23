# Better Superflat Datapack Collection for Minecraft 1.20

Tired of the boring single-biome vanilla superflat options?
Try out my Datapacks!
All of the datapacks in this collection create superflat-style world generation, but have all the biomes and structures of a regular world.
This even includes the Nether and the End dimensions! 

I've made a few different varieties of the datapack because I like giving out more options.

Version 1:
Modeled after the Classic Default Superflat preset, 1 layer of bedrock, and 3 blocks of terrain above it. No foliage*, no caves, no ores, no bodies of water. Just structures and biomes.

(img)

Version 2:
Like Version 1, but it has foliage* and bodies of water.


(img)

Version 3:
Modeled after the "Overworld" superflat preset, all the land is capped at sea-level, and foliage*, caves, ores, rivers, and oceans still generate like normal.

(img)

*Foliage means the grass, trees, plants, and flowers that would normally generate in a world. In Minecraft though, these are called "features" and also include lava pools, spawners, geodes, fire patches in the nether, etc.

This Datapack was made possible thanks to Jochen Jacobs' worldgen noise editor, Snowcapped!
Snowcapped: https://snowcapped.jacobsjo.eu
Jochen Jacobs' Github: https://github.com/jacobsjo

![image](https://github.com/Quidvio/Better-Superflat/assets/105707614/25ddc01a-0c9f-4274-9f9b-45a6c1b4b16e)

![image](https://github.com/Quidvio/Better-Superflat/assets/105707614/464efe27-a953-4321-b763-cd4f62c72590)

![image](https://github.com/Quidvio/Better-Superflat/assets/105707614/4009b334-2bd9-496f-a169-99d131e7382d)

![image](https://github.com/Quidvio/Better-Superflat/assets/105707614/9b2e85d0-8783-42af-a372-0487639c9657)

![image](https://github.com/Quidvio/Better-Superflat/assets/105707614/77f79ee2-708a-487a-8010-b7bdeccedba9)

If you have any suggested changes to this, I can upload them for you (like adding a nether roof, redesigning the end, dimension specific packs, etc.)

Here are some technical details of the Datapack for those who are curious or have a lot of Minecraft Knowledge 🤓.

Relating to the Classic Superflat Version:
-Mansions, Monuments, Strongholds, Mineshafts, End Cities, Nether Fossils (which for some reason are considered a structure in the code), all have hard-coded heights of generation, so they cannot be moved with a Datapack.
-This is why the Superflat world generates at the height that it does. If were much lower, Mansions wouldn't generate. 
  -This is also why Monuments cut through the bedrock, Strongholds and Mineshafts are under the bedrock. This presents an interesting challenge to the player, and is kind of funny.
    -Don't worry though! The true bottom of the world is at y =-64, so you can safely live, place blocks, and mine under the bedrock!
-On a similar note, Buried Treasures are hard-coded to generate a certain distance down (kind of? it's confusing) and won't generate naturally. I've solved this by recreating it as a custom structure, which has customizable heights. 
  -Because of a quirk with custom structures, Buried Treasures won't generate at the (9,9) chunk coordinate (like they normally do, if you didn't know) and instead will generate at the (0,0) chunk coordinate. 
  -Unfortunately it is very difficult to do this for the other structures mentioned above or I would do this.
-Technically, two types of foliage do generate in the "Classic Flat" preset, which are Kelp and Chorus Fruit (technically there are other End Features kept as well).
  -The significance of this is that the Advancement "A Balanced Diet" requires eating all food items. There is no other source of Chorus Fruit, and the only other source of Kelp is the Wandering Trader, which would be cumbersome. 
  -With that, All Advancements are possible given the limitations. I've put the challenge up to you to figure out how ;). Some Advancements are straight-forward, and some convoluted.
-The main reason I made the Nether generate at y = 32 was to avoid the ugly void fog at the bottom of the Nether, and also to make it in-line with the overworld/end (as they generate at y = 64, felt right to go half that).
-All of the structures that generate with a "beardifier" (function that adds generates terrain below a structure) made a big mess under the bedrock, so I removed that from all of those structures.
-One of the structures that can have it's height of generation changed is the Bastion, which I moved up slightly for the Nether.

Relating to Version 2:
-Due to the strange world-height flattening, I've partially edited the Biome Parameters to make some of the underground biomes (specifically the deep dark) generate close to how it normally would.
-It seems that Desert Temple's and Jungle Temple's generation is linked to sea-level. I had to make identical custom structures in order for them to generate.
-Nether Fossils are the same way, which is strange. I tried the custom structure approach with them, but it didn't work properly because they would generate in lava and stick out.
