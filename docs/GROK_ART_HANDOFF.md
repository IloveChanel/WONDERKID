# Grok Art Handoff

Grok is the implementation engineer. Do not redesign Wonder Kid and do not replace the approved art direction.

## First action

Inspect the entire WONDERKID repository and read:
- README.md
- docs/ART_ASSET_MANIFEST.md
- all existing Godot scenes/scripts/data definitions
- all files under assets/

Treat the repository as the source of truth.

## Art responsibility split

Michelle/ChatGPT handles generation and art direction.

Grok handles:
- integrating assets into Godot
- naming/path validation
- import settings
- sprite sheets
- animation players/state machines
- collision shapes
- pivots/anchors
- scaling
- scene placement
- asset registries
- data-driven references
- tests
- validation

Do NOT spend development time inventing replacement artwork.

## If an asset is missing

Do not guess.

Create/update docs/ART_MISSING_ASSETS.md with one entry per missing production asset.

Each entry MUST specify:
1. asset filename/path
2. exact purpose
3. static vs animated
4. exact pixel dimensions or aspect ratio
5. transparency requirement
6. number of frames
7. frame layout/order
8. pivot/anchor
9. expected world scale
10. visual description
11. whether it can be reused or must be unique
12. priority
13. the exact image-generation instruction that Michelle can use to create it

The final item must be a copy/paste-ready generation prompt. Keep the prompt narrowly scoped so one requested asset set does not accidentally redesign another system.

## Do not ask for unnecessary art

Before declaring an asset missing, check whether an existing asset can be reused safely.

Do not request:
- unique backgrounds for every puzzle
- duplicate versions of the same prop
- baked character artwork when modular layers are sufficient
- decorative art that has no gameplay purpose
- art for future systems that are explicitly out of scope

Prefer reusable modular assets.

## Character rules

The player is a modular 2D paper-doll character.

Chanel is a required companion:
- tiny 4-pound sable Pomeranian
- pocket-sized
- loving, loyal, playful, curious, brave, encouraging
- never replace Chanel with a generic dog

Character and companion animation systems must be data-driven.

## Animation rules

Animations must be represented by named states, not scattered hard-coded frame numbers.

At minimum support:
Player:
idle, walk, run, jump, interact, inspect, think, celebrate, surprised, rest/sit, turn/transition as required.

Chanel:
idle, walk, run, sit, curious, play_bow, spin, jump, sleep, shake, bark_happy, look_around, wag_tail, celebrate, comfort.

If an animation is not available yet, use a clearly named placeholder state and record the missing production asset. Do not break the state machine.

## Background/world rules

Initial world is The Meadow.

Locations:
home, forest, pond, garden, creek, bridge, village, workshop.

Use reusable tiles, props, structures, and modular scenery. Do not create a giant bespoke open-world map.

## Integration requirements

For every new art asset:
- register it in the asset registry/data layer
- use stable canonical paths
- avoid scene-specific hard-coded duplicates
- preserve the ability to swap the asset later
- verify import settings
- verify collision if needed
- verify animation playback if animated

## Testing

Every art integration change must be checked in Godot.

Test:
- asset loads
- scene loads
- animation states resolve
- missing paths fail clearly
- character remains playable
- Chanel remains playable
- world collisions remain correct
- save/load is unaffected

Do not treat a visual reference board as a production sprite sheet unless it is explicitly marked production-ready.

## Stop/report rule

After inspecting the repository and current art, report:
- what art is actually usable now
- what is reference-only
- what is missing
- what is blocking the next gameplay stage
- the exact generation prompts needed for the missing art

Do not invent missing assets and do not redesign the game.
