# Generals/Code/GameEngine/Source/GameLogic/Object/Die/RebuildHoleExposeDie.cpp

## Purpose
This file implements the `RebuildHoleExposeDie` module, which handles the creation of a rebuild hole when a structure dies. The rebuild hole can then automatically reconstruct the structure.

## Responsibilities
- Create a rebuild hole at the position of a dying structure.
- Transfer attackers from the original structure to the rebuild hole if configured.
- Start the rebuild process for the structure using the rebuild hole.

## Key Types
- `RebuildHoleExposeDieModuleData (struct)`: Stores configuration data for the rebuild hole, such as its maximum health and whether to transfer attackers.
- `RebuildHoleExposeDie (class)`: Implements the die module logic for creating a rebuild hole.

## Key Functions
### RebuildHoleExposeDie::onDie
- Purpose: Handles the death of an object by creating a rebuild hole.
- Calls:
  - `isDieApplicable`
  - `TheThingFactory->newObject`
  - `setPosition`
  - `setOrientation`
  - `setGeometryInfo`
  - `TheScriptEngine->transferObjectName`
  - `TheAI->pathfinder()->addObjectToPathfindMap`
  - `setMaxHealth`
  - `startRebuildProcess`
  - `transferAttack`

### RebuildHoleExposeDie::crc
- Purpose: Handles CRC operations for the module.
- Calls:
  - `DieModule::crc`

### RebuildHoleExposeDie::xfer
- Purpose: Handles data transfer (serialization/deserialization) for the module.
- Calls:
  - `DieModule::xfer`

### RebuildHoleExposeDie::loadPostProcess
- Purpose: Performs post-load processing for the module.
- Calls:
  - `DieModule::loadPostProcess`

## Globals
None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/Player.h"
  - "Common/PlayerList.h"
  - "Common/ThingFactory.h"
  - "Common/Xfer.h"
  - "GameLogic/AI.h"
  - "GameLogic/AIPathfind.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Module/AIUpdate.h"
  - "GameLogic/Module/BodyModule.h"
  - "GameLogic/Module/RebuildHoleBehavior.h"
  - "GameLogic/Module/RebuildHoleExposeDie.h"
  - "GameLogic/Object.h"
  - "GameLogic/ScriptEngine.h"

- External symbols used:
  - `ThePlayerList`
  - `TheThingFactory`
  - `TheScriptEngine`
  - `TheAI`
  - `TheGameLogic`
