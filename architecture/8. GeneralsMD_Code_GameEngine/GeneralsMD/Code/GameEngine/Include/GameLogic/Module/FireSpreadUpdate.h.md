# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/FireSpreadUpdate.h

## Purpose
Defines the fire spread update module for handling fire propagation between objects in the game.

## Responsibilities
- Manages fire spread logic for objects marked as aflame
- Controls timing and range of fire spread attempts
- Provides module data configuration for fire spread parameters
- Handles object creation list for ember particles

## Key Types
- **FireSpreadUpdateModuleData (Class)**: Contains configuration data for fire spread behavior (object creation list, spread delay ranges, spread range).
- **FireSpreadUpdate (Class)**: Update module that implements fire spread logic.
- **FireSpreadUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum).
- **FireSpreadUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum).

## Key Functions
### FireSpreadUpdateModuleData::buildFieldParse
- Purpose: Parses configuration data from ini files.
- Calls: Not inferable.

### FireSpreadUpdate::update
- Purpose: Updates fire spread state and attempts to spread fire to nearby objects.
- Calls: Not inferable.

### FireSpreadUpdate::startFireSpreading
- Purpose: Initiates fire spreading behavior for the attached object.
- Calls: Not inferable.

### FireSpreadUpdate::calcNextSpreadDelay
- Purpose: Calculates the delay until the next fire spread attempt.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `UpdateModule.h` (base class)
- `ObjectCreationList` (forward declaration)
- `MultiIniFieldParse` (for configuration parsing)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
- Module macro system (`MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`)
