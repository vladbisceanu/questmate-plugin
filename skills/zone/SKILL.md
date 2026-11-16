---
name: zone
description: "Complete a zone in World of Warcraft: Forever: what is left in a zone for a completionist, and the order to do it in. Use when the player asks for this about their character."
---

## Steps
1. `get_zone` for the zone, with `include` ["special", "rares", "exploration"] (and "gathering" when the player gathers). Completion is `counts.completed` out of `counts.listed` minus `notForCharacter` and `notInGame`.
2. Group what is left by place, using `at`: givers who stand together are one stop, and chains stay in order (`needs`).
3. `get_details` for each stop's quests (up to 10 references a call): objectives and where they are, so the route covers the undiscovered areas on the way.
4. `show_map` with the first stops' quest references and `route: true`; the server orders the stops to walk the least. Narrate the route in the order of the pins' `step`, and the `unexplored`, `special` and `rares` layers.

## A good answer
- Completion figures for quests and exploration, and any special quest chain or rare worth a detour (with why).
- A route by stop: quests to pick up, objectives with coordinates, turn-ins, and the areas each stop discovers.
- `needs_level`, `needs_quest` and `unclassified` quests listed as later or uncertain, never as missed.

The player's own words come first: when they ask for something different from these steps, do what they ask.
