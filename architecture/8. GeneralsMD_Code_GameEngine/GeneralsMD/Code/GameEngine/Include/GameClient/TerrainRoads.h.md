# GeneralsMD/Code/GameEngine/Include/GameClient/TerrainRoads.h

## Purpose
Defines data structures for terrain roads and bridges, including their properties, damage states, and visual effects.

## Responsibilities
- Define `TerrainRoadType` class for road/bridge descriptions
- Manage collections of roads and bridges via `TerrainRoadCollection`
- Provide accessors for road/bridge properties (textures, models, damage states)
- Support parsing from INI files via field parse tables

## Key Types
- **BridgeTowerType (Enum)**: Identifies bridge tower positions (left/right, from/to)
- **TerrainRoadType (Class)**: Stores road/bridge properties (textures, models, damage states)
- **TerrainRoadCollection (Class)**: Manages lists of roads and bridges
- **FieldParse (Class)**: Used for INI parsing (forward declared)
- **AsciiString (Class)**: String type (forward declared)

## Key Functions
### `findRoad`
- Purpose: Locates a road by name.
- Calls: None visible.

### `newRoad`
- Purpose: Allocates a new road and links it to the list.
- Calls: None visible.

### `parseTransitionToOCL` / `parseTransitionToFX`
- Purpose: INI parsing helpers for damage/repair transitions.
- Calls: INI parsing APIs (not shown in header).

## Globals
- **TheTerrainRoads (TerrainRoadCollection*)**: Global instance of the road/bridge collection.

## Dependencies
- `Common/GameMemory.h`, `Common/SubsystemInterface.h`
- `GameLogic/Module/BodyModule.h` (for `BodyDamageType`)
- `INI` class (for parsing)
- `RGBColor` (for radar color)
