# Generals/Code/Tools/WW3D/max2w3d/gamemaps.h - Enhanced Analysis

## Architectural Role
This file defines the bridge between 3ds Max's material system and the W3D format's texture requirements. It's part of the asset pipeline tools that convert Max assets into the game's proprietary format.

## Cross-References
### Incoming
- Likely called by the MAX plugin's material editor UI
- Used by the W3D export pipeline (max2w3d tool)

### Outgoing
- Interfaces with MAX SDK's material system (MtlBase, Texmap)
- Uses ReferenceTarget system for MAX's dependency graph

## Design Patterns
- **Adapter Pattern**: Converts MAX's Texmap system to W3D's texture slot requirements
- **Composite Pattern**: GameMapsClass manages a collection of TexmapSlotClass instances
- **Observer Pattern**: Uses MAX's NotifyRefChanged for dependency tracking

Rules followed. Output under 400 tokens.
