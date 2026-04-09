# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SpawnPointProductionExitUpdate.h

## Purpose
Defines a module for managing unit spawning at specific bone positions on a building.

## Responsibilities
- Manages exit points for produced units via named bones
- Tracks spawn point occupancy and availability
- Initializes bone positions in world space
- Validates occupier existence

## Key Types
- **SpawnPointProductionExitUpdateModuleData (Class)**: Holds module configuration (bone name data)
- **SpawnPointProductionExitUpdate (Class)**: Main module class implementing exit interface
- **MAX_SPAWN_POINTS (Enum)**: Defines maximum spawn points (10)

## Key Functions
### `initializeBonePositions`
- Purpose: Converts bone positions to world space coordinates
- Calls: Not inferable

### `revalidateOccupiers`
- Purpose: Clears invalid occupier IDs
- Calls: Not inferable

### `reserveDoorForExit`
- Purpose: Reserves a spawn point for unit exit
- Calls: Not inferable

### `exitObjectViaDoor`
- Purpose: Places unit at reserved spawn point
- Calls: Not inferable

## Globals
- **MAX_SPAWN_POINTS (const int)**: Maximum spawn points limit

## Dependencies
- `UpdateModule.h`, `INI.h`, `BaseType.h`
- `Object`, `Thing`, `ThingTemplate`, `ExitInterface`, `UpdateModuleData`
