# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Die/CreateObjectDie.cpp

## Purpose
Handles the creation of new objects when an object dies in the game.

## Responsibilities
- Manages the death behavior of objects to spawn new objects
- Transfers health and damage state from the dying object to the new one
- Handles transfer of attackers from the old object to the new one
- Provides serialization support for game state saving/loading

## Key Types
- `CreateObjectDieModuleData` (Class): Stores configuration data for object creation on death
- `CreateObjectDie` (Class): Implements the die module behavior for creating new objects

## Key Functions
### `CreateObjectDieModuleData::buildFieldParse`
- Purpose: Sets up field parsing for configuration data
- Calls: `DieModuleData::buildFieldParse`

### `CreateObjectDie::onDie`
- Purpose: Handles the death event and creates new objects
- Calls: `ObjectCreationList::create`, `BodyModuleInterface::attemptDamage`, `AIUpdateInterface::transferAttack`

### `CreateObjectDie::crc`
- Purpose: Generates CRC checksum for serialization
- Calls: `DieModule::crc`

### `CreateObjectDie::xfer`
- Purpose: Handles serialization of module data
- Calls: `DieModule::xfer`

## Globals
- None

## Dependencies
- `PreRTS.h`, `GameLogic/Module/AIUpdate.h`, `Common/ThingFactory.h`, `Common/Xfer.h`, `GameLogic/GameLogic.h`, `GameLogic/Module/CreateObjectDie.h`, `GameLogic/Object.h`, `GameLogic/ObjectCreationList.h`, `GameLogic/Module/BodyModule.h`
- `MultiIniFieldParse`, `INI`, `DamageInfo`, `Object`, `Thing`, `ModuleData`,
