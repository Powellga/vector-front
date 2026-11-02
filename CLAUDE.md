# Battle Zone Game

This file provides guidance to Claude Code when working with code in this repository.

## Project

**Battle Zone Game**

## Working Directory

`C:/Users/gregg/Claude-Code-IDE-Workspaces/battle-zone-game`

## Project Context Log

Claude: this section is the project's persistent memory, loaded at the start
of every session. Whenever durable project facts change during a session -
decisions made, architecture added or changed, key files, external resources
or IDs, constraints, blockers, milestones reached - update this section in
that same session, without being asked. Keep it a compact rolling summary:
fold in new facts, prune what is obsolete. Do not log routine activity.

- 2026-11-02: Gregg asked for an exact copy of Atari's Battlezone. That was declined because it would copy someone else's game. What was built instead is an ORIGINAL game in the same genre: `vector-front.html`, a single self-contained file with no assets and no outside libraries. Keep future changes original. Do not copy Battlezone's look, enemies or screen layout.
- Game design: a first-person wireframe tank game. The world is an 800x800 map that wraps around at the edges. Colors: cyan scenery, lime enemies, amber on-screen readouts (the HUD). Enemies: hover tank (1000 points), strider ramming drone (1500, from wave 2), gun tower (2500, takes 2 hits, from wave 3). A supply drone appears now and then; shooting it gives back 50 armor. Waves need 4+2*wave kills. The player gets a bonus tank every 30000 points. The HUD has a compass strip, a radar sweep, a target-lock reticle, an armor bar and side arrows that point to enemies off screen.
- All sound is generated live with the Web Audio API (engine hum, cannon, explosions, radar blips, lock tone, warning beeps, jingles). The high score is saved in the browser's localStorage under `vectorfront.hi`.
- Controls: WASD or the arrow keys, Space to fire, P to pause, M to mute, Enter to start.
- Git repo, public on GitHub: https://github.com/Powellga/vector-front (branch main, created 2026-11-02). GitHub Pages serves the game at https://powellga.github.io/vector-front/vector-front.html. README.md shows screenshots from `screenshots/` (title.png, gameplay.png), captured with headless Chrome (`--screenshot --virtual-time-budget`, with a temporary copy that sends Enter to start play).
