# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/CreateObjectDie.h

## Purpose
Defines a game module that spawns a new object when the current object dies.

## Responsibilities
- Spawns a new object upon the death of the current object
- Transfers health from the dying object to the new object if configured
- Manages module data for object creation parameters

## Key Types
- **CreateObjectDieModuleData (Class)**: Holds configuration for object creation (creation list and health transfer flag)
- **CreateObjectDie (Class)**: DieModule implementation that handles object spawning on death
- **CreateObjectDieMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **CreateObjectDie_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### CreateObjectDieModuleData::buildFieldParse
- Purpose: Parses INI configuration fields for the module data
- Calls: Not inferable

### CreateObjectDie::onDie
- Purpose: Handles the death event and spawns the new object
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Common/INI.h` (for INI parsing)
- `GameLogic/Module/DieModule.h` (base class)
- `Thing` (forward reference, game object base)
- `ObjectCreationList` (forward reference, object creation template)
- `MultiIniFieldParse` (for INI parsing)
- `Bool` (basic type)
- `DamageInfo` (damage event data)
