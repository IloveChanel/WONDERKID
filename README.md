# Wonder Kid

Wonder Kid is a family-friendly adventure + learning game built with Godot + GDScript.

## Art source of truth

The `assets/` directory contains the current Wonder Kid visual direction and reference art. Production gameplay code must keep art data-driven and replaceable.

### Important companion

Chanel is a required core companion: a tiny 4-pound sable Pomeranian, preserved in Wonder Kid as a beloved virtual companion.

### Current art status

The checked-in PNGs include concept/reference boards and separated reference crops. They are not to be treated as final production sprite atlases unless explicitly marked as such in the asset manifest.

See:
- `docs/ART_ASSET_MANIFEST.md`
- `docs/GROK_ART_HANDOFF.md`
- `assets/reference/`
- `assets/characters/`
- `assets/world/`
- `assets/props/`
- `assets/ui/`

Grok should inspect the manifest and repository before requesting additional art. If production assets are missing, Grok must report the exact asset path, dimensions/aspect ratio, transparency requirement, animation frames, naming convention, and intended use so additional assets can be generated without redesigning the game.
