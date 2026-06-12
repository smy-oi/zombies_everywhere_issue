# zombies_everywhere_issue
This repository is used for submitting issues or downloading the mod "zombieseverywhere"


Tired of the lackluster difficulty in vanilla Minecraft? Craving a truly intense and thrilling zombie apocalypse experience? **ZombiesEverywhere** is tailor\-made for you\! This mod builds a perilous, heart\-stopping zombie survival world while fully adapting to the vanilla game ecosystem\.

## Core Content Overview

### 1\. Six Unique Zombie Types

All zombies are new entities added by the mod, **with no modifications to any vanilla mob attributes**, perfectly compatible with the mod's exclusive mechanics\. Except for Regular Zombies, each special zombie type features unique particle effects\.

| Zombie Name | Basic Attributes | Special Skills \& Traits |
| --- | --- | --- |
| Normal Zombie | • Health: 20<br>• Attack: 3<br>• Speed: 0\.23<br>• Armor: 2 | No special skills; designed exclusively to fit the mod's spawn mechanics and day\-based growth system |
| Poisone Zombie | • Health: 30<br>• Attack: 4<br>• Speed: 0\.23<br>• Armor: 2 | Attacks inflict the **Poison effect** |
| FastZombie | • Health: 12<br>• Attack: 2<br>• Speed: 0\.6<br>• Armor: 2 | Raids players at ultra\-high speed—by the time it's detected, it's often too late to react |
| Burning Zombie | • Health: 30<br>• Attack: 4<br>• Speed: 0\.23<br>• Armor: 2 | Two core skills:<br>1\. **Fire Missile**: Locks onto the player, charges up, and continuously fires enhanced Blaze fireballs for several seconds \(does not ignite blocks\)<br>2\. **Enhanced Fire Missile**: Fires Wither skulls, dealing explosive damage equal to 4x its attack power \(default blast radius: 8 blocks; block destruction can be disabled via config\) |
| SummonerZombie | • Health: 20<br>• Attack: 3<br>• Speed: 0\.23<br>• Armor: 2 | 1\. Summons 5 mod Regular Zombies every 30 seconds<br>2\. Summons 1 mod Special Zombie every 40 seconds<br>3\. **Extra summons on death**: 10 Regular Zombies \+ 1 Special Zombie<br>⚠️ High risk: Mass spawning may cause game lag—beware of the "nesting doll" effect |
| EliteZombie | • Health: 75<br>• Attack: 6<br>• Speed: 0\.24<br>• Armor: 8 \(far exceeding vanilla\) | Dominant in all attributes—pure numerical strength is its greatest skill |

### 2\. Infection Mechanic

- **Trigger Condition**: Sustained attacks by zombies in a short period raise infection probability from 0 up to a **maximum of 50%**\.
  
- **Infection Effects**: Reduces the player's movement speed and maximum health\.
  
- **Level Up**: Automatically levels up by 1 every 3 minutes; being attacked again while infected also triggers a level up, with negative effects intensifying per level\.
  
- **Only Antidote**: Drinking Milk fully removes all levels of infection\.
  

### 3\. Highly Customizable Zombie Spawning System

The mod includes a built\-in independent spawner with full configuration options:

- Spawn weight for each zombie type
  
- Spawn probability per Tick
  
- Chunk range for zombie spawning around the player
  
- Whether zombies can spawn during daytime
  
- Currently a Demo\-version spawner \(biome\-specific spawn differences not yet implemented\)
  
- Default difficulty is high—casual players may need to tweak settings
  

### 4\. Dynamic Day\-Based Enhancement System

- Only applies to mod\-exclusive zombies, **no impact on vanilla mobs**\.
  
- Toggle on/off freely via config options\.
  
- Default growth rate: All attributes increase daily based on the previous day's values\.
  
- Example \(default health growth multiplier: 1\.025x\): Regular Zombie health after 5 days = 20 × 1\.025⁴ ≈ 22\.07 points
  

### 5\. Immersive Zombie\-Exclusive Mode

When enabled via config, **disables spawning of all vanilla mobs except Zombies and the Ender Dragon** \(including the Wither\), creating a pure zombie apocalypse world\.

### 6\. Balanced Full Loot System

To resolve the lack of vanilla mob drops in Zombie\-Exclusive Mode:

- Mod zombies' loot tables include **all drops from disabled vanilla mobs**\.
  
- **Dimension Balance Mechanic**: When the player is in the Nether, drop rates for Nether\-exclusive items are significantly boosted; rates for Overworld/End items are suppressed accordingly\.
  
- Limits a maximum of **3 item types** per drop \(adjust via the `max_drop_types` field in the config file\)\.
  
- Some originally guaranteed drops become probabilistic; drop rates can also be customized via Data Packs\.
  

### 7\. Infinitely Scalable Corrupted Gear System

To counter increasingly powerful zombies, the mod adds a full set of top\-tier gear with infinite enhancement potential:

#### Basic Gear

- **Corrupted Armor Set** \& **Corrupted Sword**: Crafted using Netherite gear as the base, combined with Nether Stars and the mod\-exclusive drop **Corrupted Blood**\.
  
- Basic attributes outperform the Netherite set across the board\.
  

#### Corrupted Sword Enhancement Mechanics

- **Basic Enhancement** \(Levels \+1→\+3, \+5→\+7, \+9→\+11\.\.\.\):
  
  - Recipe: Smithing Template \(top\) \+ Corrupted Sword \(middle\) \+ Corrupted Blood \(bottom\) \(positions 2, 5, 8 in the 3x3 crafting grid\)\.
    
  - Effect: Random attack damage boost \(7\.5%\~12\.5%\) per enhancement\.
    
  - Failure Penalty: Only Corrupted Blood and Smithing Template are consumed; weapon level remains unchanged\.
    
- **Enchantment Enhancement** \(Levels \+4, \+8, \+12\.\.\.\):
  
  - Recipe: Nether Star \(top\) \+ Corrupted Sword \(middle\) \+ Corrupted Blood \(bottom\)\.
    
  - Effect: Attack damage boost \+ random enchantment gain/upgrade\.
    
- **Ultimate Enhancement** \(Levels \+8, \+16, \+24\.\.\.\):
  
  - Effect: Attack damage boost \+ enchantment enhancement \+ random permanent boost to **attack damage / attack speed / attack range**\.
- **Important Note**: Enhancements have a failure chance\. If a Nether Star recipe fails, the weapon **drops 1 level** \(e\.g\., failing to upgrade from \+7 to \+8 reverts it to \+6\)\.
  
- **Current Status**: Still in Demo version, only the Corrupted Sword has implemented enhancement effects\.
  
- **Recipe Note**: Due to custom recipe return value limitations, JEI incorrectly displays this as a shapeless recipe—strictly follow the grid positions above\.
  

### 8\. Comprehensive Config Support

The mod offers extensive customization with numerous adjustable parameters:

- Basic attributes and skill parameters for all zombies
  
- Infection mechanic probability, upgrade timing, and negative effect intensity
  
- Spawning system parameters
  
- Day\-based enhancement growth rate and upper limit
  
- Gear enhancement failure mechanics
  

## ⚙️ Compatibility Notes

- For optimal compatibility, this mod does **not** use Mixin—this limits zombie enhancements to vanilla attribute caps \(e\.g\., maximum health of 1024\)\. If possible, **we highly recommend installing AttributeFix Mod alongside** to break attribute caps\.
  
- The mod automatically detects AttributeFix and configures itself—no manual adjustments required\.

