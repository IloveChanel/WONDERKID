# GROK — WONDER KID COMPLETE ART + ENGINEERING HANDOFF

You are the implementation engineer for the Wonder Kid game.

The repository is:
IloveChanel/WONDERKID

The art direction is already decided. Do NOT redesign it.

## Your first job

Inspect the entire repository before changing anything.

Read:
- README.md
- docs/ART_ASSET_MANIFEST.md
- docs/GROK_ART_HANDOFF.md
- docs/ART_MISSING_ASSETS.md
- every existing Godot scene/script/data file
- every asset currently under assets/

The repository is the source of truth.

## Critical division of responsibility

Michelle/ChatGPT is handling the artwork and image generation.

You are handling:
- Godot implementation
- asset integration
- animation systems
- asset registries
- scene integration
- collision
- pivots/anchors
- import settings
- data-driven references
- tests
- validation
- documentation

DO NOT spend time inventing new artwork.
DO NOT redesign the visual direction.
DO NOT replace Chanel.
DO NOT silently use random substitute images when a required production asset is missing.

If something is missing, tell us exactly what to generate.

## Chanel is mandatory

Wonder Kid must have Chanel as a core companion.

Chanel:
- tiny 4-pound miniature Pomeranian
- sable-colored coat
- pocket-sized appearance
- loving
- loyal
- playful
- curious
- brave
- encouraging
- comforting
- finds hidden things
- celebrates the child's successes

Chanel is based on a beloved real dog and must remain visually consistent throughout the game.

Never replace Chanel with a generic dog.

## Player character

Use a modular 2D paper-doll architecture.

Separate layers:
- body
- skin
- face
- eyes
- hair
- hair color
- tops
- bottoms
- dresses
- shoes
- hats
- accessories
- backpack

New clothing/accessory art must be addable through data/configuration without rewriting gameplay.

## Player animation states

Support named animation states, not scattered hard-coded frame numbers.

At minimum:
- idle
- walk
- run
- jump
- interact/use
- inspect/look
- think
- celebrate
- surprised
- rest/sit
- turn/transition if required by the movement implementation

## Chanel animation states

At minimum:
- idle
- walk
- run
- sit
- curious
- look_around
- play_bow
- spin
- jump
- sleep
- shake
- bark_happy
- wag_tail
- celebrate
- comfort
- discover/alert

If production animation art is not available, create the state and use a clearly named placeholder. Record the missing art.

## World

Initial world:
THE MEADOW

Locations:
1. Home
2. Forest
3. Pond
4. Garden
5. Creek
6. Bridge
7. Village
8. Workshop

Do not create a giant open world.

Use reusable modular:
- terrain
- tiles
- trees
- bushes
- flowers
- grass
- rocks
- paths
- water
- fences
- bridges
- wells
- signs
- lamps
- benches
- buildings
- workshop pieces
- garden pieces
- cooking objects
- science objects
- engineering objects
- household objects

Gameplay logic must never depend on a baked background.

## Current art

The current art establishes:
- Wonder Kid visual style
- Meadow visual direction
- modular child character direction
- Chanel direction
- environment categories
- prop categories
- UI direction
- sample character movement
- sample Chanel movement and interactions

Treat concept boards/reference images as references, not automatically as production sprites.

## Production asset requirements

Production character/companion assets should be transparent PNGs or sprite sheets with:
- consistent frame size
- consistent pivot
- consistent scale
- predictable frame order
- canonical filenames
- Godot import settings

Backgrounds should be opaque scene/background art where appropriate.

Terrain should be tileable.

Props should be reusable and separable.

## Missing-art protocol — IMPORTANT

If any required production asset is missing:

1. Do NOT guess.
2. Do NOT invent a replacement.
3. Do NOT redesign the feature.
4. Check the repository for an existing reusable equivalent.
5. If no suitable asset exists, update docs/ART_MISSING_ASSETS.md.

For EVERY missing asset, report:

- exact file path
- filename
- purpose
- static or animated
- exact pixel dimensions
- aspect ratio
- transparent or opaque
- frame count
- sprite-sheet layout
- frame order
- pivot/anchor
- expected world scale
- reusable or unique
- priority
- visual description
- exact copy/paste-ready image-generation prompt

The generation prompt must be specific enough for Michelle/ChatGPT to generate the asset without another design meeting.

## Do not over-request art

Before asking for new art, determine whether an existing asset can be reused.

Do NOT request:
- a unique background for every puzzle
- duplicate props
- duplicate characters
- baked versions of modular character parts
- decorative art with no gameplay purpose
- future art for systems not currently being implemented

Prefer reusable modular assets.

## Godot architecture

Use:
- Godot
- GDScript
- local-first storage
- data-driven asset registries
- clean interfaces so assets can be replaced later
- no Railway integration now
- no cloud account requirement now

Keep:
GAME LOGIC
ART ASSETS
LEVEL DATA
EDUCATIONAL CONTENT

separate.

Replacing art must not require gameplay rewrites.

## Testing

Test every art integration.

Verify:
- scene loads
- asset path resolves
- sprite imports
- animation state exists
- animation frames are in correct order
- character movement works
- Chanel movement works
- collision still works
- scale/pivot is correct
- save/load is unaffected
- missing asset errors are clear

Use Godot/GUT/headless tests where practical.

## Stop conditions

After the repository inspection, report exactly:

### A. Assets already usable
List exact paths.

### B. Reference-only assets
List exact paths.

### C. Missing production assets
List exact paths and specifications.

### D. Blocking assets
Identify only assets that actually block the current implementation stage.

### E. Generation instructions
Provide the exact prompts that Michelle/ChatGPT should use for every missing blocking asset.

### F. Non-blocking later art
List art that can wait.

Do not say "we need more art" without specifying exactly what art.

Do not move into unrelated future content.

Do not change the approved Wonder Kid concept.

## Final requirement

The goal is not to make a pretty mockup.

The goal is to leave the repository with a real, testable, data-driven Godot game that can consume the final art assets without architecture changes.

Inspect first. Implement second. Report missing art precisely.
