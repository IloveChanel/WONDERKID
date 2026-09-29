# Wonder Kid Art Asset Manifest

## Status
Current checked-in art is reference/concept art. Production assets must be separated into reusable sprites, backgrounds, UI, and animation resources before being treated as final.

## Required production structure

assets/
  reference/
  characters/
    player/
      body/
      skin/
      face/
      eyes/
      hair/
      hair_color/
      tops/
      bottoms/
      dresses/
      shoes/
      hats/
      accessories/
      backpacks/
      animations/
    chanel/
      base/
      expressions/
      outfits/
      accessories/
      animations/
  world/
    backgrounds/
      meadow/
      forest/
      village/
      garden/
      pond/
      creek/
      workshop/
      home/
    terrain/
    tiles/
    buildings/
    structures/
    nature/
    effects/
  props/
    cooking/
    tools/
    science/
    household/
    garden/
    engineering/
  ui/
  icons/

## Player character production set

The player must be modular 2D paper-doll art, not a single baked character.

Required layers:
- body
- skin tones
- face
- eyes
- hair styles
- hair colors
- tops
- bottoms
- dresses
- shoes
- hats
- accessories
- backpack

Required movement states:
- idle
- walk
- run
- jump
- interact/use
- inspect/look
- celebrate
- think
- gentle surprised reaction
- rest/sit
- transition/turn where required by the movement system

Animations should be delivered as transparent PNG sprite sheets or separate transparent frame PNGs, using a consistent frame size and pivot.

## Chanel production set

Chanel is mandatory.

Identity:
- tiny 4-pound miniature Pomeranian
- sable coat
- pocket-sized appearance
- loving, loyal, playful, curious, brave, encouraging

Required expressions:
- happy
- excited
- curious
- sleepy
- playful
- surprised
- thinking
- loving

Required movement:
- idle
- walk
- run
- sit
- curious/look around
- play bow
- spin
- jump
- sleep
- shake
- happy bark
- wag tail

Required interaction states:
- pet
- groom
- receive treat
- equip backpack
- change outfit
- learn trick
- comfort/hug moment
- celebrate success
- discover/alert child to something

Chanel must remain visually consistent across all states.

## World production set

Initial world: The Meadow.

Required locations:
1. home
2. forest
3. pond
4. garden
5. creek
6. bridge
7. village
8. workshop

Do not build a huge open world for V1.

Use reusable modular environment pieces:
- grass
- dirt
- stone
- path
- water
- sand
- wood
- fences
- rocks
- cliffs
- waterfalls
- trees
- bushes
- flowers
- grass clusters
- signs
- benches
- lamps
- bridges
- wells
- paths
- houses
- workshop
- market structures
- garden structures
- workshop structures

Backgrounds should be separable from gameplay logic and replaceable without rewriting scenes.

## Props

Cooking:
- apple
- carrot
- tomato
- broccoli
- bread
- egg
- milk
- cheese
- meat/protein
- bowl
- flour
- sugar
- rice
- vegetables
- fruit
- cooking tools

Engineering/tools:
- hammer
- wrench
- saw
- screwdriver
- drill
- wheelbarrow
- toolbox
- paint
- wood
- nails
- measuring tools
- bridge pieces
- pipes
- gears
- water-system pieces

Science/nature:
- magnifying glass
- binoculars
- telescope
- microscope
- compass
- specimen jars
- leaves
- rocks
- insects
- plants
- observation tools

Household:
- bed
- table
- chair
- sofa
- bookshelf
- lamp
- rug
- plant
- picture
- storage
- organization containers

## UI

Core UI references include:
- Play
- Journal
- Map
- Settings
- Adventure Energy
- coins/currency display
- backpack
- book/journal
- map
- settings
- star/discovery
- heart/companion interaction
- inventory
- simple interaction prompts

UI must remain readable, child-friendly, and consistent with the visual direction.

## Art rules

- bright, colorful, polished storybook/cartoon style
- soft rounded forms
- expressive but not visually noisy
- consistent proportions
- consistent lighting
- consistent scale
- no photorealism
- no violent imagery
- no frightening horror imagery
- no gambling/loot-box visual language
- no public social UI
- no combat UI

## Technical asset rules

Every production asset must have:
- canonical filename
- category
- intended Godot use
- pixel dimensions
- transparent/opaque requirement
- anchor/pivot guidance
- collision guidance when relevant
- animation frame count when relevant
- frame order when animated
- license/source note if not generated internally

Never hard-code an asset filename into gameplay logic when a data registry can reference it.

## Current reference boards

Current visual references were generated for:
- overall Wonder Kid visual direction
- broad Wonder Kid asset library
- Chanel companion concept

These establish the art direction and asset categories. They do not replace production-ready separated assets.

## Missing-asset reporting

If code requires an asset that is not production-ready, do NOT silently substitute a random image.

Create/update:
docs/ART_MISSING_ASSETS.md

For every missing asset report:
- exact path
- category
- purpose
- required dimensions/aspect ratio
- transparent or opaque
- animation/static
- frame count
- recommended sprite-sheet layout
- pivot/anchor
- expected scale in world
- visual description
- whether one asset or a set is required
- priority: blocker / needed / later

This report is the handoff for generating the next art batch.
