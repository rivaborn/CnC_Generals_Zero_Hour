# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/HelixContain.h

## Purpose
Defines the HelixContain module, a specialized transport container for the game.

## Responsibilities
- Manages container behavior for units/structures
- Handles damage states, capture events, and object containment
- Controls payload creation and redeployment
- Provides container UI elements (pips)

## Key Types
- **HelixContainModuleData (Class)**: Module data containing payload templates and UI flags
- **HelixContain (Class)**: Main container class extending TransportContain
- **HelixContainMagicEnum (Enum)**: Not inferable
- **HelixContain_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### onBodyDamageStateChange
- Purpose: Handles damage state transitions
- Calls: Not inferable

### onDie
- Purpose: Cleanup when container is destroyed
- Calls: Not inferable

### createPayload
- Purpose: Creates initial payload contents
- Calls: Not inferable

### getContainerPipsToShow
- Purpose: Determines UI pips visibility
- Calls: ContainModuleInterface::getContainerPipsToShow

## Globals
- **None**

## Dependencies
- TransportContain.h
- MultiIniFieldParse, INI, AsciiString, Bool, Object, Player, DamageInfo, ObjectID, ModuleData classes
- std::vector, std::vector::const_iterator
