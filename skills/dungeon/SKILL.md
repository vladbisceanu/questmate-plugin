---
name: dungeon
description: "Prepare for a dungeon in World of Warcraft: Forever: whether the character is ready for a dungeon, what to bring, and the quests to take in. Use when the player asks for this about their character."
---

## Steps
1. The dungeon's reference: from `get_next_steps` `dungeons`, or `find` with its name.
2. `get_details` with that reference: group-finder levels, entrance, nearest flight master, each boss's loot (stats, drop chance, `usableFrom`, and `upgrade` when it beats what the character wears) and its quests with the character's status.
3. Gear: loot with `upgrade` is worth hoping for. For upgrades from other sources before going in, `get_gear_plan` with levels ahead up to the dungeon's range.
4. Quests: those `available` to pick up before going in, and for `needs_quest` ones the earlier quest; `get_details` on their references gives givers and places.
5. `show_map` for the dungeon's zone with its reference and the quests to pick up in `refs`, and the `flights` layer.

6. Supplies: `find` with `need` "ammo" (for hunters) or "class_reagents", and "pet_food" with the pet's family, for the nearest vendors.

## A good answer
- Ready or not, against the group-finder range; the data gives no separate entry level, so do not state one.
- The loot worth hoping for, by slot, compared with what the character wears, with drop chances and when it becomes usable.
- Quests to take in, in the order to get them, and the route to the entrance.
- Supplies for the class (food, drink, bandages, ammunition, pet food) and repairs.
- Boss tactics, if wanted, with their source: the dungeon's ForeverDB `url` or the web.

The player's own words come first: when they ask for something different from these steps, do what they ask.
