NB: ship sprites are not original, and are placeholders only. Please do not distribute this work-in-progress plug-in in this condition.


# Trin Enhancement for Endless Sky

## The Trin

The Trin are a proposed hostile, Tier 3 alien species. I'm designing them with the following objectives:

1. Provide a late game challenge for an experienced player's fleet, which makes a bit more story sense than farming the Quarg.
2. Offer a great range of outfits: weapons that might compete with the Quarg Skylance, and other outfits balanced to the Wanderers/Korath.
3. To be relatively ‘low impact’ in terms of territory and storyline. Their territory is long lost, and their planned stories try to fit into the existing setting.
4. To push the boat out mechanically: their missiles shoot bomb-pumped lasers, their Matrix Guns do more damage the closer they hit, a rare ship variant creates illusions of itself, and more...


## Background

They raid the galactic north from the Wanderers to the Korath, checked by the Quarg in Hai and Efreti space. The Trin were once an advanced civilisation, a long time ago. They rose to a great height, but their continued warring became ever more dangerous. Eventually, their atrocities caught the attention of the Drak, who sought to contain the threat.

The Trin refused all conditions of surrender, and while they were no match for the Drak and the Quarg, they fought an endless guerrilla war. Their civilisation was lost, but their Trin Fabricators (molecular assemblers) and underground hives helped them seed themselves across the galaxy and fight back. They bloodied the Quarg in battle, and even injured a few Archons.

Eventually, the Drak lost patience. They fell back on an ultimate sanction: a weapon that completely destroyed all intelligent Trin life.

They miscalculated. Trin civilisation was composed of two halves. The true Trin were intelligent and civilised, and the Drak’s weapon killed every one. Their drones are strong and obedient: good at performing a given task but with no autonomy of their own. The Drak’s weapon did not affect the Trin drones. Millenia have passed, and Trin drones continue to fulfill their dead Queens’ dying wishes for war.

They seed new hives on uninhabited worlds, build new ships, and attack with no concept of free will, strategy, or mercy. They no longer recognise enemy or civilian. They’re a mindless husk of a dead species, fighting a war that’s already lost: a galactic pest. The Drak task the Quarg with eradicating hives before they ‘hatch’, and defending the Hai and Efreti from the few Trin that reach them. Despite their advanced technology, this has been enough to keep the fallen Trin mostly in check.

At least, so far.


## Gameplay

The Trin have no fleet presence. They appear through rare, usually invisible ‘raid’ missions. In Hai and Efreti space, Quarg will show up to help – eventually.

1. 8 new Tier 3 ships: Piranha fighters, Raja interceptors, Marlin light warships, Chimaera medium warships, Cachalot heavy freighters and Mako, Mobula and Antiarch heavy warships. Only the first three can realistically be captured.
2. 7-12 new weapons: Phase Reapers, Matrix Guns/Batteries, Stasis Snares, Hunter-Killer Pods, Hunter-Seeker Pods and the mighty Arcblade. More rarely you’ll find Phase Reaper Turrets, Empyreal Fields, Wakefield Mortars, Hunter-Trapper Pods and Warp Cascades. 
3. 16 new outfits, including competitive alternatives to Wanderer/Korath reactors, Wanderer regenerators, Korath/Coalition cooling, Quarg batteries and Hai engines. Plus some other cool stuff.
4. The Mebsuta Hive arc, a 10 mission arc encountering a mysterious alien threat under the worst circumstances.
5. The Hai Research arc, a 9 mission arc investigating the technology and origin of the Trin. Also repeating Hai missions warning of Trin raids once your combat rating is high enough.
6. The Wanderer Defence arc, about 6 missions dealing with a Trin hive.
7. The Trin Queen arc, about 4 missions finding out much more about the Trin’s origin, from a very different perspective.
8. The Dreadhand’s Challenge, a 2 mission story where you can respond to (or ignore) a challenge from an infamous pirate lord with some pretty unusual technology.

## Code Dependencies

**_[STABLE]_** **[Dev/Trin](https://github.com/Elyssaen/endless-sky/tree/dev/trin)** – a combined branch of all relatively stable features / code dependencies. Feel free to compile this and have a look around. I'll make pre-compiled executables available at some point, but in the long run the hope is that all code dependencies can be accepted into Endless Sky.

1. _**[MERGED]**_ **[OperationalEnergy](https://github.com/Elyssaen/endless-sky/tree/feature/OperationalEnergy)** - rather than having negative energy generation, an outfit that should constantly drain energy now uses positive "operational energy". This is needed to fix some incompatibilities with solar collection, and also to make it possible to equip Strangelet Adapters before reactors. (Update: this functionality has made it into the core game.)
2. _**[MERGED]**_ **[ExcessiveSpeedDecay](https://github.com/Elyssaen/endless-sky/tree/feature/ExcessiveSpeedDecay)** – ships cannot obtain limitless speed when using a weapon with firing force to thrust. Needed to balance the Warp Cascade. (Update: this functionality has made it into the core game, albeit not through this specific branch.)
3. _**[DONE]**_  **[RangeCalculation](https://github.com/Elyssaen/endless-sky/tree/feature/RangeCalculation)** – a tweak to Endless Sky’s range calculation to handle random lifetime/velocity and submunition velocity, needed to get certain Trin weapons (like the Phase Reaper and Arcblade) to be used effectively by the AI. 
4. _**[DONE]**_  **[NoCollision](https://github.com/Elyssaen/endless-sky/tree/feature/NoCollision)** – a new weapon attribute that allows for munitions that don’t hit anything, needed for proper operation of some fancy Trin weapons (like the Empyreal Field and Arcblade).
5. _**[DONE]**_  **[EffectResistances](https://github.com/Elyssaen/endless-sky/tree/feature/EffectResistances)** – Trin shield regenerators provide resistance to disruption and piercing damage. (The branch also creates slowing and ion resistance, not used by the Trin.)
6. _**[DONE]**_  **[MoreJammingTypes](https://github.com/Elyssaen/endless-sky/tree/feature/MoreJammingTypes)** – creates optical, infrared and untyped jamming, as the Trin use a fancy Tier 3 jammer. (Untyped not used.)
7. _**[DONE]**_  **[ShipsConditions](https://github.com/Elyssaen/endless-sky/tree/feature/ShipsConditions)** – ability to key a mission off your fleet size is used in the Dreadhand’s Challenge.
8. _**[DONE]**_ **[TurretFiringArc](https://github.com/Elyssaen/endless-sky/tree/feature/TurretFiringArc)** – any weapon (turret or gun) can have a "swivel degrees" attribute, allowing it to swivel within that range. Needed so that Swivel Matrix Guns can fire in a +/- 30 degree arc.
9. _**[DONE]**_  **[OutfitTags](https://github.com/Elyssaen/endless-sky/tree/feature/OutfitTags)** – any outfit or ship can have tags, and they will automatically be turned into auto-conditions that can be used for mission logic. Needed for the Trin Queen arc to trigger on having _any_ piece of Trin technology in your fleet.
10. _**[TESTING]**_  **[JammingHaywire](https://github.com/Elyssaen/endless-sky/tree/feature/JammingHaywire)** – to make jammers effective in AI-on-AI combat at Tier 3, this makes it possible to ‘confuse’ jammed missiles into veering off.
11. _**[PLANNED]**_ **MoreJammingHaywire** – combination of MoreJammingTypes and JammingHaywire.
12. _**[PLANNED]**_ **GiftShip** – a feature to let a mission give you a ship, needed for a mission reward.
13. _**[NO IDEA YET]**_  **SpriteTransparency** – Trin jammers need to make the ship equipping them translucent.
14. _**[PLANNED]**_ **MissionLandmark** - mission creation enhancement: ability to define a location filter and then use the result multiple times. Needed for right handling of a Trin raid: the Trin should appear in a random system, and so too should the Quarg.
15. _**[PLANNED]**_ **NPCTravelTo** - mission creation enhancement: an NPC can be defined with orders to travel to a fixed location. Needed for handling of a Trin raid: the Quarg should travel to the location of the raid and then stay there.