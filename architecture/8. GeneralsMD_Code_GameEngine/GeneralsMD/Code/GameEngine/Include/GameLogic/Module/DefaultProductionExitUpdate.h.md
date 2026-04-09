# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/DefaultProductionExitUpdate.h

## Purpose
Defines a module for handling unit production exits in the game, managing how units spawn from buildings.

## Responsibilities
- Manages unit exit logic from production structures
- Handles rally points and exit positions
- Provides interface for door-based exits and budding
- Configurable via INI data for unit creation points

## Key Types
- **DefaultProductionExitUpdateModuleData (Class)**: Stores configuration data for exit behavior
- **DefaultProductionExitUpdate (Class)**: Implements the exit update module logic
- **DefaultProductionExitUpdateMagicEnum (Enum)**: Not inferable
- **DefaultProductionExitUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### `DefaultProductionExitUpdateModuleData::buildFieldParse`
- Purpose: Registers INI field parsing for module data
- Calls: `UpdateModuleData::buildFieldParse`

### `DefaultProductionExitUpdate::exitObjectViaDoor`
- Purpose: Handles unit exit through a door
- Calls: Not inferable

### `DefaultProductionExitUpdate::setRallyPoint`
- Purpose: Sets the rally point for exiting units
- Calls: None

### `DefaultProductionExitUpdate::getRallyPoint`
- Purpose: Retrieves the rally point if it exists
- Calls: None

### `DefaultProductionExitUpdate::useSpawnRallyPoint`
- Purpose: Checks if spawn units should use rally points
- Calls: None

## Globals
- None

## Dependencies
- `UpdateModule.h`
- `Common/INI.h`
- `Lib/BaseType.h`
- `Object` class
- `UpdateModuleData` class
- `ExitInterface` interface
- `ThingTemplate` class
- `Thing` class
- `MultiIniFieldParse
