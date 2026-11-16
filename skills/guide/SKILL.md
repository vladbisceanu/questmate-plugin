---
name: guide
description: "Follow a guide in World of Warcraft: Forever: make a guide the player's plan for a character: its talents, and its link to come back to. Use when the player asks for this about their character."
---

## Steps
1. `get_plan`: what the character already follows (guide, talent build, goal).
2. Read the guide's page (web): its class and spec, the goal it is for (levelling, dungeons or PvP), and its talents. A levelling guide often gives talents by level; take the build it ends with for the level the player is heading to, and say which.
3. Show the player what you found before saving: the guide's title, its goal, and the talents by tree with ranks. If the page cannot be read or gives no talents, say so; save the guide's link alone if the player wants.
4. On their yes:
   - `set_preference` with `guide`: the page's link as value, its title as name.
   - `set_preference` with `talentBuild`: the talents as a list of names and ranks (or the guide's ForeverDB calculator link as value), name the build after the guide, and source with the guide's link and title. The server checks the build the way the game does; if it refuses, say what it named and ask before changing anything.
   - `set_preference` with `goal` when the guide is for one.
5. `show_talents` with `build: "current"` only if the player wants to see it.

## A good answer
- What was saved, from which guide, and where the next talent points go now.
- What the guide covers beyond talents (priorities, rotation, gear) and that you will read it from its link when that comes up: the server keeps the link, not the guide's text.
- Said once: a guide written for another version of the game (Classic, retail) may name talents Forever changed; the server's check catches talents that do not exist here.

The player's own words come first: when they ask for something different from these steps, do what they ask.
