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


# AI WORK ALLOCATION — COST CONTROL

Use a 90/10 workflow.

## GROK — TARGET 90%

Grok should complete approximately 90% of the implementation and integration work, including:
- project structure
- Godot scenes
- GDScript systems
- data models and registries
- asset loading/integration
- animation state machines
- placeholder integration
- world construction
- reusable environment setup
- character integration
- Chanel integration
- UI implementation
- save/load
- local data
- gameplay systems
- adventure framework
- educational content framework
- tests
- validation
- documentation
- bug fixes
- missing-art inventory
- exact art-generation specifications

Do not leave ordinary implementation work for Claude merely because it is tedious. Complete it in Grok whenever it can be done reliably.

## CLAUDE — TARGET 10%

Claude should be reserved for high-value finishing work after Grok has reached approximately 80–90% completion.

Use Claude primarily for:
- difficult architectural review
- complex bugs Grok cannot resolve
- final code review
- edge-case testing/reasoning
- performance review
- security/privacy review where applicable
- difficult Godot problems
- final integration polish
- identifying subtle omissions
- final quality-control pass

Do NOT send Claude the entire project just to redo work Grok has already completed.

## HANDOFF RULE

Grok must leave the project in a clean, documented state before Claude is brought in.

When Grok believes the project is approximately 80–90% complete, create:
`docs/CLAUDE_FINAL_REVIEW.md`

That document must contain:
1. what is complete
2. what was tested
3. what remains
4. known bugs
5. known limitations
6. architecture decisions
7. files Claude should inspect
8. specific questions Claude should answer
9. exact areas where final polish is needed

Claude is a finisher/reviewer, not the primary builder.

The objective is to get the maximum amount of complete Wonder Kid functionality from Grok while reserving Claude's more expensive usage for work where deeper review or reasoning adds meaningful value.


# FINAL COMPLETION / QA WORKFLOW — REQUIRED

This project uses a three-gate completion process.

## GATE 1 — GROK IMPLEMENTATION: 80–90%

Grok is responsible for getting Wonder Kid to approximately 80–90% implementation completeness.

Grok must:
- build the systems
- connect the systems
- integrate available art
- use placeholders where final art is not yet available
- implement the gameplay framework
- implement the Meadow
- implement the player
- implement Chanel
- implement animations/state machines
- implement UI
- implement save/load
- implement the adventure framework
- implement education/content data structures
- implement energy
- implement inventory/data systems required by the current scope
- implement two-player foundation where currently required
- implement journal/world-state foundations
- write tests
- run tests
- fix ordinary bugs
- document known limitations

Grok must NOT stop at a pretty prototype.

Grok must leave the project structurally complete enough that Claude can test and finish it without rebuilding the architecture.

### Grok completion report

Before handing off to Claude, create/update:
docs/GROK_COMPLETION_REPORT.md

Include:
- implemented systems
- implemented scenes
- implemented gameplay loops
- implemented character systems
- implemented Chanel systems
- implemented animation systems
- implemented save/load
- implemented UI
- tests run
- tests passed
- known failures
- placeholders remaining
- missing art
- known technical debt
- exact files Claude should inspect

Do not claim 90% merely because many files exist. Completion means working, connected functionality.

---

# GATE 2 — CLAUDE COMPLETE INTEGRATION + QA: 100%

Claude is NOT the second developer rebuilding Wonder Kid.

Claude is the final integration engineer, test engineer, architecture verifier, and release-quality reviewer.

Claude's job is to take Grok's approximately 80–90% implementation and bring the project to a verified 100% completion state for the defined V1 scope.

## 1. TEST EVERYTHING

Run the full automated test suite.

Run headless tests where practical.

Run integration tests.

Run save/load tests.

Run data validation.

Run asset/path validation.

Run scene-loading validation.

Run animation/state validation.

Run gameplay-flow validation.

Run error/edge-case tests.

Fix failures rather than merely reporting them when the fix is within the current V1 scope.

## 2. VERIFY ARCHITECTURE

Verify that the architecture is actually connected end-to-end.

Check:
- game boot
- main menu
- world loading
- player spawning
- character data
- modular character assembly
- movement
- interaction system
- Chanel spawning/following/interactions
- animation state machines
- asset registry
- world state
- adventure framework
- educational content data
- energy system
- inventory/data systems
- journal
- save/load
- settings
- parent area foundations
- two-player foundation where implemented
- local data provider
- future provider interface
- scene transitions
- error handling

Do not accept dead code, disconnected systems, fake buttons, placeholder APIs that are supposed to be functional, or features that appear complete but do nothing.

## 3. VERIFY ART INTEGRATION

Check every production-ready asset currently in the repository.

Verify:
- paths
- imports
- dimensions
- transparency
- pivots
- anchors
- animation frame order
- scale
- collision
- scene placement
- naming
- asset registry references

If art is missing, do not block unrelated systems. Use the approved placeholder architecture and document the exact missing production asset.

## 4. VERIFY THE COMPLETE CORE LOOP

The following must work from a clean launch:

START GAME
→ HOME / MAIN MENU
→ CHARACTER
→ MEADOW
→ MOVE
→ EXPLORE
→ INTERACT
→ CHOOSE / REASON
→ ADVENTURE SYSTEM
→ RESULT / CONSEQUENCE
→ JOURNAL / DISCOVERY
→ WORLD STATE
→ SAVE
→ EXIT
→ REOPEN
→ LOAD
→ CONTINUE

Test this as an actual user flow, not just individual functions.

## 5. VERIFY CHANEL

Chanel must:
- load correctly
- appear correctly
- move correctly
- animate correctly
- follow/interact correctly
- respond to supported interactions
- save/load correctly
- remain visually consistent

Chanel cannot be treated as optional content.

## 6. VERIFY FAILURE AND RECOVERY

Test what happens when:
- an asset is missing
- save data is absent
- save data is malformed
- a scene fails to load
- an invalid content ID is encountered
- an animation is unavailable
- a player exits mid-flow
- a puzzle/adventure is restarted

The game should fail safely and recover where appropriate.

## 7. VERIFY PERFORMANCE

Check for:
- unnecessary memory growth
- repeated asset loading
- runaway processes
- excessive scene duplication
- animation/state leaks
- obvious frame-rate problems
- save/load stalls
- input problems

Fix clear issues within scope.

## 8. CREATE THE 100% RELEASE VERIFICATION REPORT

Create:
docs/CLAUDE_FINAL_REVIEW.md

It must contain:

### A. SYSTEMS VERIFIED
Every V1 system and whether it works.

### B. TESTS RUN
Every automated/manual test category.

### C. FAILURES FOUND
What failed and why.

### D. FIXES MADE
What Claude fixed.

### E. REMAINING NON-BLOCKING ITEMS
Only genuinely non-blocking items.

### F. MISSING ART
Exact production assets still needed.

### G. RELEASE BLOCKERS
Anything that must be fixed before phone testing.

### H. PHONE TEST RECOMMENDATION
The exact phone test sequence to use next.

### I. FINAL STATUS
Use one of:
- NOT READY
- READY FOR PHONE TEST
- READY FOR RELEASE CANDIDATE

Do NOT call the project 100% complete merely because tests pass. Architecture and actual end-to-end functionality must also be verified.

---

# GATE 3 — PHONE TEST: REPRESENTATIVE, NOT EVERY LEVEL

We do NOT manually play every adventure/level on the phone before moving forward.

The purpose of phone testing is to verify that the real build works on the target device and that representative gameplay flows survive the actual mobile environment.

Use a risk-based representative test matrix.

## PHONE SMOKE TEST

First verify:
- install/build
- launch
- loading
- orientation
- touch input
- menus
- settings
- character screen
- Meadow
- movement
- interaction
- Chanel
- save
- exit
- relaunch
- load

## REPRESENTATIVE GAMEPLAY TESTS

Manually test a small representative sample covering different system types rather than every level.

At minimum cover:
1. one exploration/nature activity
2. one engineering/physics activity
3. one logic/reasoning activity
4. one multi-step activity
5. one cooking/math/budgeting activity once that system is available
6. one world-state-changing activity
7. one two-player flow once two-player is available

The exact final sample can be selected from the implemented adventures based on risk and system coverage.

## PHONE TEST RULE

If the representative tests pass and automated/integration tests cover the remaining content, do NOT manually replay every level just for the sake of checking every level.

Instead verify that all adventures use the same validated adventure framework and data contracts.

Then perform targeted manual tests on any adventure that uses a unique system or unique code path.

This is the required strategy for keeping phone QA efficient while still protecting the game from systemic failures.

---

# DEFINITION OF 100%

For this project, 100% means:

- all defined V1 architecture exists
- all defined V1 systems are connected
- all defined V1 core flows work
- automated tests pass
- integration tests pass
- save/load works
- assets are correctly integrated
- missing production art is explicitly documented
- Chanel works
- the Meadow works
- representative adventures work
- no known release-blocking bugs remain
- Claude has completed the final architecture and QA review
- the project is explicitly marked READY FOR PHONE TEST

100% does NOT mean every future feature is built.

100% does NOT mean every future world exists.

100% does NOT mean every possible cosmetic exists.

100% means the defined V1 foundation and agreed launch scope are complete, connected, tested, and ready for the next validation gate.
