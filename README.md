# Better Superflat Datapack Collection for Minecraft 1.20 (Page WIP)

Tired of the boring single-biome vanilla superflat options?
Try out my Datapacks!
All of the datapacks in this collection create superflat-style world generation, but have all the biomes and structures of a regular world.
This even includes the Nether and the End dimensions! 

I've made a few different varieties of the datapack because I like giving out more options.

## Version 1:
Modeled after the Classic Default Superflat preset; 3 layers of terrain, one layer of bedrock. No foliage[^1], no caves, no ores, no bodies of water. Just structures and biomes.

![image](https://github.com/Quidvio/Better-Superflat-Datapacks/assets/105707614/d81be696-5c3e-42d9-a50a-1f7a3edb2b48)

![image](https://github.com/Quidvio/Better-Superflat-Datapacks/assets/105707614/b492b571-a7a5-467a-8de6-629dac9df25b)

![image](https://github.com/Quidvio/Better-Superflat-Datapacks/assets/105707614/aae4e032-2fba-4e81-8119-73131e2e13ac)

![image](https://github.com/Quidvio/Better-Superflat-Datapacks/assets/105707614/1179e612-1e43-4ce4-9423-28cb9133376e)

![image](https://github.com/Quidvio/Better-Superflat-Datapacks/assets/105707614/1991470e-91a9-4e57-82cd-90be218a16ec)

![image](https://github.com/Quidvio/Better-Superflat-Datapacks/assets/105707614/a46fdac3-33d6-4673-810f-0c901d441fc4)

![image](https://github.com/Quidvio/Better-Superflat-Datapacks/assets/105707614/6e1bd23a-4151-48f8-b0b1-a5a0fa8ae7ca)

![image](https://github.com/Quidvio/Better-Superflat-Datapacks/assets/105707614/bcf8dbf1-8653-4565-8383-cada8482f843)

![image](https://github.com/Quidvio/Better-Superflat-Datapacks/assets/105707614/10e01662-0d3d-44f4-9b7f-ff8c4e01e5c3)

## Version 2:
Like Version 1, but it has foliage[^1] and bodies of water.

![image](https://github.com/Quidvio/Better-Superflat-Datapacks/assets/105707614/d0c1350f-9d1f-46e4-a885-cf145215176c)

![image](https://github.com/Quidvio/Better-Superflat-Datapacks/assets/105707614/2a50fb65-c548-4d82-893e-bf3ae2188324)

![image](https://github.com/Quidvio/Better-Superflat-Datapacks/assets/105707614/7ec717c7-0a71-4ae5-85d5-7b68ba91cbc5)

![image](https://github.com/Quidvio/Better-Superflat-Datapacks/assets/105707614/10b03050-b954-426b-8969-0500984e38b6)

## Version 3:
Modeled after the "Overworld" superflat preset; all the land is capped at sea-level. Foliage[^1], caves, ores, rivers, and oceans still generate like normal.

![image](https://github.com/Quidvio/Better-Superflat/assets/105707614/25ddc01a-0c9f-4274-9f9b-45a6c1b4b16e)

![image](https://github.com/Quidvio/Better-Superflat/assets/105707614/464efe27-a953-4321-b763-cd4f62c72590)

![image](https://github.com/Quidvio/Better-Superflat/assets/105707614/4009b334-2bd9-496f-a169-99d131e7382d)

![image](https://github.com/Quidvio/Better-Superflat/assets/105707614/9b2e85d0-8783-42af-a372-0487639c9657)

![image](https://github.com/Quidvio/Better-Superflat/assets/105707614/77f79ee2-708a-487a-8010-b7bdeccedba9)

[^1]: Foliage means the grass, trees, plants, and flowers that would normally generate in a world. In Minecraft though, these are called "features" and also include lava pools, spawners, geodes, fire patches in the nether, etc.

This Datapack was made possible thanks to Jochen Jacobs' worldgen noise editor, Snowcapped!

Snowcapped: https://snowcapped.jacobsjo.eu
Jochen Jacobs' Github: https://github.com/jacobsjo

If you have any suggested changes to this, I can upload them for you (like adding a nether roof, redesigning the end, dimension specific packs, etc.)

# Technical Details of the Datapack

## Relating to the Classic Superflat Versions:
* Mansions, Monuments, Strongholds, Mineshafts, End Cities and Nether Fossils[^2], all have hard-coded heights of generation, so they cannot be moved with a Datapack.  
  * This is why the Superflat world generates at the height that it does. If were much lower, Mansions wouldn't generate.
  * This is also why Monuments cut through the bedrock, Strongholds and Mineshafts are under the bedrock. This presents an interesting challenge to the player, and is kind of funny.
    * Don't worry though! The true bottom of the world is at y =-64, so you can safely live, place blocks, and mine under the bedrock!
* On a similar note, Buried Treasures are hard-coded to generate a certain distance down (kind of? it's confusing) and won't generate naturally. I've solved this by recreating it as a custom structure, which has customizable heights. 
  * Because of a quirk with custom structures, Buried Treasures won't generate at the (9,9) chunk coordinate (like they normally do, if you didn't know) and instead will generate at the (0,0) chunk coordinate. 
  * Unfortunately it is very difficult to do this for the other structures mentioned above or I would do this.
* Technically, two types of foliage do generate in the "Classic Flat" preset, which are Kelp and Chorus Fruit (technically there are other End Features kept as well).
  * The significance of this is that the Advancement "A Balanced Diet" requires eating all food items. There is no other source of Chorus Fruit, and the only other source of Kelp is the Wandering Trader, which would be cumbersome.
  * With that, All Advancements are possible given the limitations. I've put the challenge up to you to figure out how ;). Some Advancements are straight-forward, and some convoluted.
* The main reason I made the Nether generate at y = 32 was to avoid the ugly void fog at the bottom of the Nether, and also to make it in-line with the overworld/end (as they generate at y = 64, felt right to go half that).
  * Additionally, that meant that Nether Ruined Portals wouldn't float (Again, unable to change height of generation).
* All of the structures that generate with a "beardifier" (function that adds generates terrain below a structure) made a big mess under the bedrock, so I removed that from all of those structures.
* One of the structures that can have it's height of generation changed is the Bastion, which I moved up slightly for the Nether.
* For some reason, stopping flowers from generating also stops them from being generated with bonemeal, even though this isn't true in the nether...

## Relating to Version 3:
* Due to the strange world-height flattening, I've partially edited the Biome Parameters to make some of the underground biomes (specifically the deep dark) generate close to how it normally would.
* It seems that Desert Temple's and Jungle Temple's generation is linked to sea-level. I had to make identical custom structures in order for them to generate.
* Nether Fossils are the same way, which is strange. I tried the custom structure approach with them, but it didn't work properly because they would generate in lava and stick out.

[^2]: Nether Fossils are for some reason are considered a structure in the code.
