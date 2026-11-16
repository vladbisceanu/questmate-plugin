---
name: session
description: "Plan a play session in World of Warcraft: Forever: what to do in the next one to three hours, from where the character is now. Use when the player asks for this about their character."
---

## Steps
1. `get_plan` for the player's choices (focus, thoroughness, guide, build). Character: level, gold, logout location and snapshot time (`get_character`, unless this conversation has it). `get_progress` with `since: "last_talk"` for what they played since you last talked, session by session; open with it in a line or two when there is something.
2. `get_next_steps`: abilities to train, unspent talent points with where they go toward the build the coach follows (`talents.build`: the player's saved build, else ForeverDB's editorial pick for the spec and goal; `show_talents` with `build: "current"` draws it), zones that fit, quests available nearby, dungeons in range, and from level 20 how to play the spec (simulated advice; say so). `where.players` is a sample size; with a handful of players, treat the zone shares as a hint.
3. Pick one zone: the logout zone if it fits the level, else the nearest fit. `get_zone` with `show: "available"` for the route, and `show: "left"` when `needs_level` quests unlocking within two levels or `needs_quest` blockers matter.
4. `get_details` for the quests on the route (up to 10 references a call): objectives, where each objective is, turn-ins and rewards.
5. `show_map` for the zone with the route's quest references and `route: true`, which orders them to walk the least; give the route in the pins' `step` order, and the `flights` or `unexplored` layers when they help.
6. Only if the player is levelling a profession: `get_profession_plan`, and fold gathering or cheap crafts into the route.

## A good answer
- An ordered route: training, pick-ups grouped by where givers stand, objectives with coordinates, turn-ins, where to sell and repair.
- Says which steps depend on what the data cannot see: bags, objective progress, abilities already trained.
- Gives levels or gold gained only when the data supports it.

The player's own words come first: when they ask for something different from these steps, do what they ask.
