# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/QueueProductionExitUpdate.h

## Purpose
Manages queued unit production exits for buildings, controlling timing and positioning of spawned units.

## Responsibilities
- Handles delayed unit exits from production structures
- Manages rally points and exit positions
- Controls door reservation and object budding
- Implements exit interface for production management

## Key Types
- **QueueProductionExitUpdateModuleData (Class)**: Holds configuration data for exit behavior (positions, delays, etc.)
- **QueueProductionExitUpdate (Class)**: Main module handling queued exits and production timing
- **QueueProductionExitUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **ExitInterface**: Interface for exit management (inherited)

## Key Functions
### `reserveDoorForExit`
- Purpose: Reserve an exit door for a specific unit type
- Calls: Not inferable

### `exitObjectViaDoor`
- Purpose: Spawn a unit through a reserved exit door
- Calls: Not inferable

### `exitObjectByBudding`
- Purpose: Create a unit via budding (attached to host)
- Calls: Not inferable

### `update`
- Purpose: Update production exit timing and state
- Calls: Not inferable

### `isFreeToExit`
- Purpose: Check if production exit is available
- Calls: Not inferable

## Globals
- None

## Dependencies
- `UpdateModule.h` (base class)
- `INI.h` (for configuration parsing)
- `BaseType.h` (basic types)
- `Thing`, `ThingTemplate`, `Object` classes (game entities)
