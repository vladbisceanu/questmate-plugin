---
name: profession
description: "Level a profession in World of Warcraft: Forever: the cheapest way to raise a profession, what to buy and where to train. Use when the player asks for this about their character."
---

## Steps
1. `get_profession_plan` with the profession and the player's target skill; without a target it plans to the current rank's cap.
2. If `stuckAt` is set: `get_professions` with the profession and `known: "unknown"` for recipes that drop or come from quests past that skill.
3. Gathering professions (Skinning, Mining, Herbalism) and Fishing have no plan: level them by gathering in zones that fit the character's level and skill.

## A good answer
- The steps as a table: skill range, recipe, crafts, how to learn it and its cost, cost of the step.
- The shopping list with each item's source and the total, against `gold`; when short, the amount missing and which steps to do first.
- The nearest trainer, and when the next rank must be trained (`assumptions`).
- Skill-up chances follow the Classic rule; thresholds marked as Classic data are named as such.

The player's own words come first: when they ask for something different from these steps, do what they ask.
