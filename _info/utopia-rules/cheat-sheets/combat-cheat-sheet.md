---
layout: page
title: Combat
summary: Summarized rules for combat.
topic: Cheat Sheets
tags:
    - utopia
    - rules
    - cheat-sheet
---

## Turn Action and Interrupt Action Points
Action Points are the temporal resource used to perform actions in turn-based initiative.

### Turn Actions 🔴🔴🔴🔴🔴🔴
On each of their turns, a character receives 6 Turn Actions to spend on various abilities. Each of these points loosely corresponds to one second of real time.

### Interrupt Actions 🟢🟢
On each other character's turn, a character receives 2 Interrupt Actions to spend on various reaction abilities.

## Actions

### Travel
<b>AP Cost:</b> 🔴

Spend one AP to move up to your character's [Speed] in meters. Movement cannot be split, and unused movement does not carry over to future Travel actions or turns.

### Melee Attack
<b>AP Cost:</b> <i>Variable</i>

Spend AP based on the weapon used for the attack to deal damage based on the weapon's damage rating.

#### Weaponless Attacks
<b>AP Cost:</b> 🔴🔴

Spend 2 AP to make an unarmed attack, dealing 1d8 + [Power Mod] Physical damage.

#### Multi-Weapon Attacks
<b>AP Cost:</b> <i>Max of Used Weapons</i>

Spend AP based on the highest AP cost of the weapons used to make the multi-weapon attack. The damage rolls for all involved weapons are halved (rounded down) before being summed together.

### Ranged Attack
<b>AP Cost:</b> <i>Variable</i>
<b>Short Range:</b> 4d6 + [Dex Mod]
<b>Long Range:</b> 2d6 + [Dex Mod]

Spend AP based on the weapon used for the attack and make a to-hit roll based on the weapon's range band. On a successful hit, deal damage based on the weapon's damage ratinge. To-hit rolls are always versus the distance to target, with short range rolls having a point of favor and long range rolls having a point of disfavor.

### Aim
<b>AP Cost:</b> 🔴

Spend 1 AP to gain a point of favor on a Ranged Attack to-hit roll immediately following this action.

### Deep Breath
<b>AP Cost:</b> 🔴

Spend 1 AP to regain 1 point of Stamina.

### Leap
<b>AP Cost:</b> 🔴🔴🔴 <br>
<b>Stamina Cost:</b> 3

Spend 3 AP and 3 Stamina to jump a distance up to your [Power] in meters. If immediately preceeded by a Travel action, jump up to your [Strength] in meters instead.

### Scale
<b>AP Cost:</b> 🔴🔴🔴 <br>
<b>Stamina Cost:</b> 4
<b>Break AP Cost:</b> 🔴🔴 / 🟢

Spend 3 AP and 4 Stamina to initiate a climb against an adjacent target of equal or greater size. Make an [Agility] vs [Strength] contest if they are the same size, or an [Agility] vs [Agility] contest if the target is larger. The scaling character receives a point of disfavor for each size larger the target is.

While scaled, a character's Attack, Block, and Dodge actions requires twice as much AP if targeting the scaling character. If scaling character's weight surpasses the target's carry capacity, the target becomes encumbered.

The scaled character may spend AP once per turn to compel another contested scale roll to shake off the scaler. The scaling character expends 2 Stamina if they choose to make the roll.

### Grapple
<b>AP Cost:</b> 🔴🔴🔴 <br>
<b>Stamina Cost:</b> 2
<b>Break AP Cost:</b> 🔴🔴 / 🟢
<b>Break Stamina Cost:</b> 2

Spend 3 AP and 2 Stamina to initiate a grapple against an adjacent target. Make a contested [Strength] vs [Strength]/[Agility] check, with a point of disfavor for each size difference.

While grappled a character cannot use the Travel action, and all Attack, Block, and Dodge actions are made with a point of disfavor against any target other than the grappler. When the grappler moves the grappled character is moved along with them, but the grappler moves at 1/2 speed.

The grappled character may spend AP once per turn to compel another contested grapple roll to break free. Both characters who make the roll must expend 2 Stamina.

### Hold Action
<b>AP Cost:</b> 🔴 / 🔴🔴
<b>Activation Cost:</b> 🟢

Spend up to 2 AP to hold an action of corresponding cost. A held action may be released as a single Interrupt Action.

### Block
<b>AP Cost:</b> 🔴 / 🟢

In response to damage, spend on AP to attempt to reduce the incoming damage. Make a [Block] check against the incoming damage. Reduce the incoming damage by the result of the check.

### Dodge
<b>AP Cost:</b> 🔴 / 🟢

In response to damage, spend one AP to attempt to avoid the attack entirely. Make a [Dodge] check against the incoming damage. If the result meets or exceeds the damage, the attack is avoided. Otherwise, the character takes the damage as normal.

### Take Cover
<b>AP Cost:</b> 🔴 / 🟢 <br>
<b>Condition:</b> Suitable Cover Available

In response to damage, spend one AP to gain a point of favor on Block or Dodge checks for the rest of the turn.

### Assist
<b>AP Cost:</b> 🟢 / 🟢🟢

When another character within range takes an applicable action, spend up to 2 Interrupt AP to enhance the effects of their action.

#### Assist Block/Dodge
<b>AP Cost:</b> 🟢

When an adjacent character is making a Block/Dodge check, spend 1 AP to grant them a point of favor on the check.

#### Assist Leap
<b>AP Cost:</b> 🟢

When an adjacent character is taking a Leap action, spend 1 AP to increase their Leap distance by your [Power] score.

#### Assist Grapple
<b>AP Cost:</b> 🟢🟢

When an adjacent character is making a Grapple check, spend 2 AP to perform a [Strength] roll and add the result to their Grapple check.

#### Assist Test (Generic)
<b>AP Cost:</b> 🟢

When a character is making a skill roll, spend 1 AP to either add a point of favor to their roll or perform a corresponding skill roll and add the result to their roll. Maximum range, conditions, and effects are determined by the nature of the skill being used.

Examples:
- Aid another character in scouting: Spend 1 AP to give them a point of favor on their [Awareness] test.
- Aid another character in lifting a heavy crate: Spend 1 AP to make a [Strength] roll and add the result to their [Strength] test.

### Stealth (Partial Homebrew)
<b>AP Cost:</b> N/A

Stealth itself is not an action, but a state which requires successive [Stunt] vs [Awareness] contests to remain inconspicuous. A character may attempt to enter stealth only if they are not currently observed.

While remaining inconspicuous, a character's Attack actions gain a point of favor.

After taking any suspicious or aggressive action, a character attempting to remain inconspicuous must make a [Stunt] vs [Awareness] contest to avoid being detected. Various effects may impose favor/disfavor on this context.
- 1 Disfavor: Any character is suspicious of the character's presence.
- 1 Disfavor: Any character has seen you behaving suspiciously.
- 2 Disfavor: Any character has line of sight to you.
- 1 Favor: Terrain or circumstance provides concealment.

## Links

- Back to Info index: [Info]({{ "/info/" | relative_url }})
