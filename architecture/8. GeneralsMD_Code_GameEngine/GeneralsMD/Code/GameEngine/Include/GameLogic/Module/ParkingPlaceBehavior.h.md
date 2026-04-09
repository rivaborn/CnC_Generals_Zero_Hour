# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ParkingPlaceBehavior.h

## Purpose
Defines the `ParkingPlaceBehavior` module for managing parking spaces, runways, and healing for units in the game.

## Responsibilities
- Manages parking spaces, runways, and healing for units.
- Handles unit entry/exit via doors and rally points.
- Tracks reserved spaces and runways for units.
- Updates healing status for parked units.
- Provides interface for querying parking availability and reservations.

## Key Types
- **ParkingPlaceBehaviorModuleData (Class)**: Configuration data for parking behavior (healing, grid layout, runway flags).
- **ParkingPlaceBehavior (Class)**: Core behavior module implementing parking logic, exit management, and healing.
- **ParkingPlaceBehaviorMagicEnum (Enum)**: Not inferable (empty enum).
- **ParkingPlaceBehavior_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty enum).
- **ParkingPlaceInfo (Class)**: Stores data for a single parking space (position, orientation, occupancy).
- **RunwayInfo (Class)**: Tracks runway usage (start/end points, reservation status).
- **HealingInfo (Class)**: Records healing progress for a unit (ID and start frame).

## Key Functions
### `reserveDoorForExit`
- Purpose: Reserves a door for unit exit.
- Calls: Not inferable (implementation in .cpp).

### `exitObjectViaDoor`
- Purpose: Exits a unit through a reserved door.
- Calls: Not inferable.

### `update`
- Purpose: Updates healing and parking state.
- Calls: `purgeDead`, `resetWakeFrame`.

### `onDie`
- Purpose: Handles cleanup when the parking structure is destroyed.
- Calls: `killAllParkedUnits`.

### `buildInfo`
- Purpose: Initializes parking space and runway data.
- Calls: Not inferable.

### `purgeDead`
- Purpose: Removes references to dead units.
- Calls: Not inferable.

## Globals
- None.

## Dependencies
- `BehaviorModule.h`, `DieModule.h`, `UpdateModule.h`
- `MultiIniFieldParse`, `INI` (for config parsing)
- `Thing`, `Object`, `Team`, `Coord3D`, `ObjectID`, `ExitDoorType` (external types)
