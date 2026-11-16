---
name: pet
description: "Tame a hunter pet in World of Warcraft: Forever: which beast to tame for the hunter's level and goals, and where to find it. Use when the player asks for this about their character."
---

## Steps
1. The hunter's level (`get_character`, unless this conversation has it) and what the pet is for: levelling alone, tanking, damage in groups, or a look. Ask if the player has not said.
2. `find` with a family or beast name ("Bear", "Cat", "Wolf", "Owl") for the beasts' references, then `get_details` on the likely ones: family, levels, attack speed, where each is seen (places, whether seen in Forever), diet and the family's abilities by level.
3. A hunter can tame a beast up to its own level. Prefer beasts seen in Forever, near the character.

## A good answer
- One recommendation with the zone and coordinates, and an alternative from another family when the trade-off is close.
- The family's trade-off for the player's goal, the abilities it learns as it levels, and its diet.
- What it eats and the nearest food vendor: `find` with `need` "pet_food" and its family.
- Blizzard does not show the hunter's current pet: ask before comparing with it.

The player's own words come first: when they ask for something different from these steps, do what they ask.
