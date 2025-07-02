# LOR-qol-mods
Archive of QoL mods I've created for Library of Ruina

.dll files are openable with dnSpy. I coded each mod's applicable namesake dll file, you can use them as reference or implement them or whatever. HarmonyLib is used for patching. The images are property of ProjectMoon and are from the game files, I did not make those, obviously.

**-Battle**
Patches RencounterManager so that all phases of the system trigger at once, instead of having to sequentially wait for each phase to end. Most noticeably is that the attack will trigger at the same time as the dice rolling. There are a few other possible implementations of this, such as speeding up and reducing the delay of the attacks themselves, or enabling the Ro/Ar toggle which automatically ends each phase as fast as possible, but those have their own flaws. (UI still takes forever for the former, while in the latter, you don't get to see the rolling or vanilla dice).

**-BattleUnitLight**
Fixes unit light so you can have more than 2 rows of 5 light. While the original did work with more than 10 light, it would put extra light onto the bottom row only and then eventually break. I did have a few variations of this one that had more than 2 rows, but I think 2 rows is simplest.

**-Buff**
Adds icons to text references to buffs. There are a few hardcoded name changes, such as Bleeding to Bleed (the actual buff doesn't have a a reference to the text version name) or Immobilized to Stun. I'm not proud of how I implemented this one, but it works.

**-Card**
Increases the length of the card viewers. Also moves the close/open page toggles to the other side. Now, they end up in the same place no matter if you're opening or closing them, and they aren't near the start combat button so you can't do a woopsie.

**-Damage**
Adds Icons to damage types. There's a damage type for most of the xml/code versions in the game, like passives, bufs, card abilities, etc. There were pictures suited for those, but not for Emotion/Card abilities, so I scrounged the files for something. Technically replaceable if you replace them with images with the same file name, but whether or not the size is correct is up to your own discretion.
**The images themselves are the property of ProjectMoon. I didn't make those, etc.**

**-EquipPageLight**
Adds a light/max light counter to equip pages. Doesn't entirely stay consistent, might fix later. Do note it states current light + 1/max light, since units recover 1 light at the beginning of each Scene, but it is possible to change this to be 0 light, in which case this counter becomes incorrect. While there technically is a way to check this, it's too much work for me.
**Images are property of ProjectMoon, same as above.**

**-HandSize**
Allows the display of more than 1 row of cards. Each row has 9 cards. Display does not exceed 1 row when hovering over a unit (otherwise you can't even select units). Upon picking a card, all cards go to the bottom so you can see better. Do note that units have their own max draw and max hand size, and nothing in the vanilla game should exceed 9, so this usually only works with other mods, but those other mods probably either don't use 9+ cards or have their own patch if they do.
