# Agent Skill: Utopia Creature Crafter

This agent skill is designed to assist users in creating custom creatures using the Utopia TTRPG rule set digitized in `_info/utopia-rules/custom-creature-creation/`.

## 1. Creature Creation Workflow

When a user wants to create a creature, follow this strict process:

### Phase 1: Modular Assembly
1.  **Select Body**: Exactly one Body must be chosen (e.g., Beast, Humanoid). This sets the Base Difficulty Rating (DR).
2.  **Select Kits**: Any number of Kits may be added (e.g., Tank, Evasive). These increase stats and DR.
3.  **Select Classes**:
    *   Max 1 Martial Class (e.g., Brute).
    *   Max 1 Arcane Class (e.g., Necromancer).
    *   Max 1 Support Class (e.g., Healer).
    *   Max 1 of *each* Innate Class (e.g., Skyborn).
    *   Classes increase stats, DR, and provide Actions/Equipment.

### Phase 2: Stat Calculation
Start with the **Body's Base Stats** and add modifiers from **Kits** and **Classes**.
*   **Attributes**: SHP, DHP, Stamina.
*   **Defenses**: Physical, Energy, Heat, Chill, Psyche.
*   **Subtraits**: Speed, Power, Dexterity, Fortitude, Resolve, Awareness, Engineering, etc.
*   **Travel**: Land, Water, Air (Note: specific rules like Skyborn override these).
*   **Avoidance**: Dodge Rating (Dice), Block Rating (Dice).

### Phase 3: Final Calculations
1.  **Difficulty Rating (DR)**: Sum the `Base DR` (Body) + `Added DR` (Kits/Classes).
2.  **Loot Rarity**: Determined by Final DR (unless Body specifies otherwise):
    *   **< 20**: Crude
    *   **20 - 39**: Common
    *   **40 - 74**: Extraordinary
    *   **75 - 149**: Rare
    *   **150 - 299**: Legendary
    *   **300+**: Mythical
3.  **Harvest Quantity & Type**: Determined by Body (e.g., Beast gives `1d6 material`).

### Phase 4: Output Generation
Generate a Markdown file content block using the following template:

```markdown
---
layout: creature
title: <Creature Name>
type: <Body Type>
kits: [<List of Kits>]
classes: [<List of Classes>]
dr: <Final DR>
---

# <Creature Name>

**<Rarity> <Body Type>** (DR: <Final DR>)

*Harvest: <Harvest Dice> <Component Type>*

## Description
<Flavor text>

## Stats

| Stat | Value | | Defense | Value |
| :--- | :--- | | :--- | :--- |
| **SHP** | <Total SHP> | | **Physical** | <Phys Def> |
| **DHP** | <Total DHP> | | **Energy** | <Eng Def> |
| **Stamina** | <Total Stam> | | **Heat/Chill** | <Heat>/<Chill> |
| **Travel** | <L>/<W>/<A> | | **Psyche** | <Psy Def> |

**Subtraits:**

|   **Speed:** <Speed> | **Dexterity:** <Dex> | **Power:** <Pow>
|   **Fortitude:** <Fort> | **Resolve:** <Res> | **Awareness:** <Awa>
(List others if > 1)

**Avoidance:**
*   **Dodge:** <Dodge Dice>
*   **Block:** <Block Dice>

## Abilities & Traits
*   **<Trait Name> (Source):** <Effect Description>

## Actions
*   **<Action Name> (<Cost> Actions):** <Range> range. <Damage Dice> <Type> damage. <Effect>.
```

## 2. Reference: Creature Type Mapping

| Type | File Path |
| :--- | :--- |
| **Overview (Loot)** | `00-overview.md` |
| **Bodies** | `01-creature-bodies.md` |
| **Kits** | `02-kits.md` |
| **Martial Classes** | `03-martial-classes.md` |
| **Arcane Classes** | `04-arcane-classes.md` |
| **Support Classes** | `05-support-classes.md` |
| **Innate Classes** | `06-innate-classes.md` |
