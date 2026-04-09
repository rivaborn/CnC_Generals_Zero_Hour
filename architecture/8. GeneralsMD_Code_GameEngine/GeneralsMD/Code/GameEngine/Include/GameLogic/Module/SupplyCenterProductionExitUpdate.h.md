# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SupplyCenterProductionExitUpdate.h

## Purpose
Manages unit exit behavior from supply centers, handling rally points and exit positions.

## Responsibilities
- Controls unit exiting via doors or budding
- Manages rally points for produced units
- Provides exit position and natural rally point queries
- Handles temporary stealth grants for exiting units

## Key Types
- **SupplyCenterProductionExitUpdateModuleData (Class)**: Holds module configuration (create point, rally point, stealth frames).
- **SupplyCenterProductionExitUpdate (Class)**: Implements exit logic and rally point management.
- **SupplyCenterProductionExitUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum).
- **ExitInterface**: Interface for exit behavior (inherited).

## Key Functions
### `exitObjectViaDoor`
- Purpose: Exits an object through a specified door.
- Calls: Not inferable (implementation in .cpp).

### `setRallyPoint`
- Purpose: Sets the rally point for exiting units.
- Calls: None.

### `getRallyPoint`
- Purpose: Retrieves the rally point if it exists.
- Calls: None.

### `update`
- Purpose: Module update loop (always sleeps forever).
- Calls: None.

## Globals
- None.

## Dependencies
- `UpdateModule.h` (base class)
- `MultiIniFieldParse`, `INI` (INI parsing)
- `ThingTemplate`, `Object`, `Thing` (game entities)
- `Coord3D` (3D coordinates)
- `ExitInterface` (exit behavior interface)
