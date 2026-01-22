# Agent Skill: Utopia Item Crafter

This agent skill is designed to assist users in creating custom items using the Utopia TTRPG rule set digitized in `_info/utopia-rules/custom-item-creation/`.

## 1. Item Creation Workflow

When a user wants to create an item, follow this strict process:

### Phase 1: Identification & Context
1.  Determine the **Item Type** (e.g., Fast Weapon, Shield, Consumable).
2.  **Read** the specific rule file associated with that type found in `_info/utopia-rules/custom-item-creation/`.
3.  **Read** `_info/utopia-rules/custom-item-creation/00-general-crafting-rules.md` for base Rarity/Time tables.

### Phase 2: Feature Assembly
1.  Start with **Innate Stats** (Base RP, Base Slots, Base Hands).
2.  Add **selected features**. 
    *   Check if feature is **Stackable**. If not, ensure count is 1.
    *   Check **Compatibility** notes (e.g., "Not compatible with Concealed").
    *   Sum the **RP modifiers** (Positive adds RP, Negative subtracts RP).
3.  Ensure the item does not exceed **Feature Count Limits** based on resulting rarity.

### Phase 3: Calculation Engine
1.  **Total RP Calculation**: Sum of all feature RP costs. (If < 1, set to 1).
2.  **Rarity Determination**:
    *   **Crude**: 0-20 RP
    *   **Common**: 21-40 RP
    *   **Extraordinary**: 41-70 RP
    *   **Rare**: 71-110 RP
    *   **Legendary**: 111-160 RP
    *   **Mythical**: 161-220 RP
3.  **Value Calculation**:
    *   **Crude**: RP (Min 2)
    *   **Common**: RP x 2 (Min 10)
    *   **Extraordinary**: RP x 4 (Min 40)
    *   **Rare**: RP x 8 (Min 160)
    *   **Legendary**: RP x 16 (Min 560)
    *   **Mythical**: RP x 32 (Min 1760)
4.  **Crafting Time**:
    *   Use the table in `00-general-crafting-rules.md`.
5.  **Component Cost Calculation**:
    *   **Standard Items (Weapons/Armor)**: 
        *   Usually determined by specific feature costs (e.g., "+1 Material Component"). *Agent must read specific file entries.*
    *   **Consumables**: 
        *   1 Power / 50 RP (Min 1)
        *   1 Refinement / 40 RP (Min 1)
    *   **Artifacts**:
        *   1 Power / 50 RP (Min 0)
        *   1 Refinement / 40 RP (Min 1)
        *   1 Material / 25 RP (Min 1)
    *   *Always round down component calculations.*

### Phase 4: Output Generation
Generate a Markdown file content block (no need to save unless asked) using the following template:

```markdown
---
layout: item
title: <Item Name>
type: <Item Type>
rarity: <Calculated Rarity>
value: <Calculated Value>
components:
  power: <Count>
  refinement: <Count>
  material: <Count>
stats:
  hands: <Count>
  slots: <Count>
  damage: <Dice> <Type> # If weapon
  range: <Range> # If weapon
  block: <Rating> # If shield
  dodge: <Rating> # If shield
features:
  - name: <Feature Name>
    cost: <RP cost>
    effect: <Summary of effect>
---

# <Item Name>

**<Rarity> <Item Type>**
*Crafting Time: <Time> | Value: <Value> SC | RP: <Total RP>*

## Description
<Flavor text or description>

## Stats
*   **Hands:** <Hands>
*   **Slots:** <Slots>
*   **Range/Defense:** <Stats>

## Features
*   **<Feature Name> (+<RP> RP):** <Effect Description>
```

## 2. Reference: Item Type Mapping

| Item Type | File Path |
| :--- | :--- |
| General Rules | `00-general-crafting-rules.md` |
| Fast Weapon | `01-fast-weapons.md` |
| Moderate Weapon | `02-moderate-weapons.md` |
| Slow Weapon | `03-slow-weapons.md` |
| Shield | `04-shields.md` |
| Chest Armor | `05-chest-armor.md` |
| Head Armor | `06-head-armor.md` |
| Hand Armor | `07-hand-armor.md` |
| Foot Armor | `08-foot-armor.md` |
| Consumable | `09-consumables.md` |
| Artifact | `10-artifacts.md` |

## 3. Component Calculation Rules (Fallback)

If the specific item file does not specify component formulas (like Weapons/Armor often imply per-feature costs), use the standard logic:
*   Most **Physical** features cost **Material Components**.
*   Most **Magical/Elemental** features cost **Power Components**.
*   Most **Utility/Speed** features cost **Refinement Components**.
*   *Note: Detailed component costs for weapons/armor appear in the feature descriptions (e.g., "Requires 1 Material Component"). The Agent must parse this from the text.*
