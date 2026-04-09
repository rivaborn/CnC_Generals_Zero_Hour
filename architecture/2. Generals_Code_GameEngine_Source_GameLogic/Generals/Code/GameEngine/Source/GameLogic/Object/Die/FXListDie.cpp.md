# Generals/Code/GameEngine/Source/GameLogic/Object/Die/FXListDie.cpp

## Purpose
This file implements the `FXListDie` class, which handles the death effects for game objects in Command & Conquer Generals.

## Responsibilities
- Handles the die callback for objects.
- Manages default death effects and ambient sound stopping.
- Implements CRC and Xfer methods for data serialization.

## Key Types
- FXListDie (Class): Handles death effects for objects.
- FXListDieModuleData (Struct): Stores module-specific data for death effects.

## Key Functions
### onDie
- Purpose: Triggers the default death effect when an object dies.
- Calls: `isDieApplicable`, `getFXListDieModuleData`, `TheAudio->stopAllAmbientsBy`, `FXList::doFXObj`, `FXList::doFXPos`

### crc
- Purpose: Implements CRC method for data integrity checks.
- Calls: `DieModule::crc`

### xfer
- Purpose: Handles data serialization and deserialization.
- Calls: `xfer->xferVersion`, `DieModule::xfer`

### loadPostProcess
- Purpose: Performs post-processing after loading.
- Calls: `DieModule::loadPostProcess`

## Globals
None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/INI.h"
  - "Common/ThingTemplate.h"
  - "Common/Xfer.h"
  - "GameClient/FXList.h"
  - "GameLogic/Damage.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/FXListDie.h"
  - "GameLogic/Module/AIUpdate.h"

- External symbols:
  - `TheAudio`
  - `TheGameLogic`
