# Assorted-Adjustments
A selection of tweaks for Beamdog's Enhanced Editions for the Baldur's Gate and Icewind Dale games.


### Berserker Enrage Disables Spellcasting

A straight nerf. Prevents Wizard spells, Priest spells, and magical innates. Allows non-magical abilities and item usage.

### Minsc Remains Controllable While Using His Berserk Ability

A straight buff. The Berserk status effect (which normally makes Minsc uncontrollable) is removed, and the +2 to hit and damage bonus the Berserk status effect would normally grant is separately included. Spellcasting is disabled, as with the Berserker component.

### Berserk Override Script For Minsc

Gives Minsc an override script (that is, a script that takes precedence of his normal companion AI and works even with companion AI turned off) that simulates the original berserking behavior. He will automatically equip a melee weapon and attack the nearest enemy. He can be given orders, but he'll shortly ignore them and resume mindlessly attacking. However, he won't attack friendlies, and you have enough control over him to use the fastest actions (such as chugging a potion).

### Make sleep end upon taking damage

Sleeping targets wake up when they're damaged, as one would expect. Sleep is still very powerful, but not an auto-win/loss.

### Make unconsciousness NOT end upon taking damage

Unconscious targets stay unconscious despite being damaged. Mostly a fix for IWD:EE, in which, according to the spell descriptions, this should already be the case (but isn't). 

### PnP Skull Trap

Skull Trap does 2d4 + (1d4*level) damage, only affects living creatures, and has a casting time of 4 instead of 3. The changes are taken from AD&D 2nd Edition source material, and make the spell more distinct from (and maybe not as clearly always superior to) Fireball.

### Cure Spells Won't Affect Undead And Constructs

According to PnP rules (and common sense, IMO), Cure spells should not affect the non-living.

### Consistent Charm Person (or Mammal): Doesn't Turn Neutral Characters Hostile

Makes the regular "Charm" spells work like the Ring of Human Influence, Algernon's Cloak and Nymph Cloak: characters that were neutral (blue circle) when charmed remain neutral when the charm ends. Dire Charm, Domination and such are conceptually different, and still turn their targets hostile when they end.

### Fixes For Deities of Faerûn

Fixes some bugs with spell functionality in the Deities of Faerûn mod: 

- Tyr Cleric's Detect Invisibility works at will, not once per day
- Holy Word special ability is party friendly (only needed for for IWD:EE)
- Strength of One special ability does not override strength higher than 18/76

Needs to be installed after DoF.

### SCS Rules For Deities of Faerûn Cleric Antimagic (Can Target Invisible)

Compatibility patch for users of Sword Coast Stratagems and Deities of Faerûn. Makes the Priest variants of antimagic spells granted by DOF behave like their wizard equivalents do under SCS.

### Deafness prevents hearing Rogue Rebalancing bard song

The Enhanced Editions have had Bard song be prevented by deafness, as well as break invisibility, for a long time. Rogue Rebalancing, however, hasn't been updated for it. Atweaks has a component that adds the second functionality. This adds the first. Requires RR Bard class changes (and is obviously pointless without it).

### Prevent Mislead clones from being able to attack when speed weapons are equipped

Mislead clones are illusionary, and aren't supposed to be able to affect ther physical world. BG:EE accomplishes this by setting their attacks per round to zero, but the effect doesn't cover speed weapons: a Mislead clone of someone wielding Belm will still get the extra attack from the sword. This component fixes that.

### Allow Mislead clones to play Bard songs


On the other hand, Mislead clones are explicitly able to speak, so singing shouldn't be an issue either.


### Stop Free Action from preventing beneficial effects 


Makes it so Free Action doesn't "protect" against spells like Haste. Also fixes some nonsensical interactions with Blade spins, which it shouldn't interact with at all. Unlike (at the time of this writing) the klatu fix, this one works with the EE Fixpack. Quite possibly redundant since the release of a cdtweaks component that does the same.

### Remove Monk Haste Immunity 

By request.

### Restful Cabins

Does it grind your gears to not be able to rest in an empty cabin in the wilds, but somehow being perfectly able to camp in the yard? This allows resting in some such places (currently the cabins in Cloakwood and the High Hedge).

### Give IWD Dispel Magic a chance to succeed/fail based on caster level like in Baldur's Gate

In Icewind Dale, Dispel (and Remove) Magic has a 100% success chance, which makes it quite overpowered, renders all other antimagic spells redundant, and is incorrect by PnP rules. This component changes it to behave like the BG version, with a chance to dispel based on caster level and the effect being targeted.

### NPC Sprites

Give Pit Fiends their Neverwinter Nights sprite animation
Give Succubi their Neverwinter Nights sprite animation
Give Bone Fiends a Neverwinter Nights sprite animation
Give Hamatula their Neverwinter Nights sprite animation
Give Abishai their Icewind Dale / Siege of Dragonspear sprite animation
Give Alu-Fiends wings
Give Erinyes wings (and change their sprites from human to elf)
Give Displacer Beasts their Neverwinter Nights sprite animation
Give Viconia her Sharran character colors from Siege of Dragonspear in BG1/BG2
Give Voghiln a more warrior-like appearance by giving him the Fighter animation and basic chain mail as his starting armor

These are purely cosmetic changes, and fairly self-evident. The credit for most of these animations goes to the Infinity Animations mod, though some of the devils were scaled down a bit from that mod's baseline.

### Give Belhifet a Custom Portrait

A custom portrait I created for Belhifet, initially from an AI prompt, then painting over the result, then compositing the result with some stock photos, then running the whole thing through a different AI, then compositing again, then hand painting again, et cetera. I think it actually looks lore accurate, but in any event it took too much effort not to share somewhere. Includes a portrait for the mysterious voice Hephernaan communicates with, as well.

<img width="2375" height="1347" alt="Belhifet" src="https://github.com/user-attachments/assets/e074d45b-dc2d-4f41-8365-35b6c1ba813e" />

### Lazy Companion AI 

This AI is meant to automate tasks that are repetitive, trivial, or otherwise unfun, and to prevent them from deciding to do things you probably don't want them to. It's not meant to be anywhere near smart enough to play the game for you.

Characters can be set to automatically attack enemies they see. They will then attack the nearest enemy they see that their equipped weapon can affect. Characters wielding melee weapons will not attack fire shielded enemies unless they have 100% resistance to the fire shield's damage type. Characters wielding ranged weapons will automatically switch to melee when attacked by in close quarters combat and then back to ranged once the enemy is gone. The combat AI will not target NPCs classified as innocent, like civilians who might have become hostile as the result of a failed pickpocketing.

For Clerics and Paladins, auto-attacking will be automatically disabled while Turn Undead is enabled.

Thieves will default to detecting traps when idle. They will stop and attack when enemies are encountered, but manually turning trap detection back on in combat will disable auto-attacking until detection is manually turned off again. This is so that you can try to dispel illusions in combat without always having to toggle auto-attacking or disable the AI.

Bards can be set to activate their song when entering combat, or to sing constantly when idle. Both  are suspended while invisible.  When set to sing constantly and with auto-attacking on, the battlesong will behave the same as  trap detection for thieves.

Hotkeys:

"A" 	Toggle automatically attacking enemies. (Note that "A" is also the default AI hotkey, I recommend rebinding it.)
"S" 	Switch to melee weapons
"D" 	Switch to ranged weapons (these two keys only switch between equipped sets, they do not set an AI preference)
"G" 	Switch between Detecting Traps / Stealth. For Bards, toggle when Bard Song should be up.

"E" 	Make selected characters go through their healing spells from least to most powerful (up to Cure Serious Wounds)
		to heal both themselves and nearby companions. Characters will not try to heal companions who are invisible or
		have deflection spells active. This healing routine only triggers out of combat.

Automatic buffing: selected characters will automatically cast common defensive spells, starting with themselves and continuing with nearby party members. Separated by duration to avoid situations where one character's short duration buffs are already expiring before another is even through casting the long duration ones. As with healing, this is an out of combat routine, and characters will not try to heal companions who are invisible or have deflection spells active.

"X" 	Cast extremely long duration buffs (such as stoneskin)
"C" 	Cast long duration (turn/level) buffs
"V" 	Cast medium duration (multiple rounds per level) buffs
"B" 	Cast short duration (one round per level or less) buffs
"N" 	Cast deflection-type spell defenses on self. Separate because these spells prevent being further buffed by others.

Includes Icewind Dale spells, if installed, and some (but not all) of the spells and abilities from Deities of Faerûn.
