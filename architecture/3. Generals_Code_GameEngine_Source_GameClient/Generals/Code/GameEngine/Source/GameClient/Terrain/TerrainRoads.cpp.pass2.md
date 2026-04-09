# Generals/Code/GameEngine/Source/GameClient/Terrain/TerrainRoads.cpp - Enhanced Analysis

## Architectural Role
This file implements the data model and parsing logic for terrain roads and bridges, serving as the bridge between INI configuration and runtime terrain rendering. It's part of the terrain subsystem but also tightly coupled with the object/body damage system for bridge damage states.

## Cross-References
### Incoming
- Terrain rendering system (uses road/bridge definitions)
- Object/body damage system (for bridge damage state transitions)
- INI parsing infrastructure (calls parseTransitionToOCL/parseTransitionToFX)

### Outgoing
- Common/INI.h (for configuration parsing)
- Body damage system (references BodyDamageType)
- Memory allocation (newInstance)

## Design Patterns
- **Factory Pattern**: `newRoad`/`newBridge` methods create and initialize road/bridge instances
- **Composite Pattern**: `TerrainRoadCollection` maintains lists of road/bridge types
- **Strategy Pattern**: Field parsing uses strategy objects (FieldParse table) for configuration loading

Rules followed. Output under 400 tokens.
