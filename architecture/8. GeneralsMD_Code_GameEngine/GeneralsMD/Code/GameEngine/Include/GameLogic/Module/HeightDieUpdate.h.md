# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/HeightDieUpdate.h

## Purpose
Defines a game module that destroys objects when they reach a specified height above terrain.

## Responsibilities
- Manages height-based destruction logic for game objects
- Handles particle system cleanup at specified heights
- Tracks object movement direction for conditional destruction
- Provides module data configuration for height thresholds

## Key Types
- **HeightDieUpdateModuleData (Class)**: Configuration data for height-based destruction
- **HeightDieUpdate (Class)**: Module implementing height-based destruction logic
- **HeightDieUpdateMagicEnum (Enum)**: Not inferable
- **HeightDieUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### HeightDieUpdateModuleData/buildFieldParse
- Purpose: Parses configuration data from game files
- Calls: Not inferable

### HeightDieUpdate/update
- Purpose: Updates destruction logic each frame
- Calls: Not inferable

## Globals
- None

## Dependencies
- `UpdateModule.h` (base class)
- `MultiIniFieldParse` (for configuration parsing)
- Memory pool management macros
- Standard module macros for game engine integration
