# Generals/Code/GameEngine/Source/GameLogic/Object/Behavior/POWTruckBehavior.cpp

## Purpose
This file implements the behavior for POW trucks in Command & Conquer Generals, handling interactions with surrendered units.

## Responsibilities
- Manages POW truck behavior.
- Handles collisions with surrendered units.
- Implements CRC and Xfer methods for data serialization.

## Key Types
- `POWTruckBehaviorModuleData (struct)`: Data structure for POW truck behavior module.
- `POWTruckBehavior (class)`: Class implementing POW truck behavior logic.

## Key Functions
### onCollide
- Purpose: Handles collisions with other objects, specifically picking up surrendered units.
- Calls: 
  - `getObject()`
  - `getAIUpdateInterface()`
  - `isSurrendered()`
  - `loadPrisoner()`

### crc
- Purpose: Implements CRC method for data integrity checks.
- Calls: 
  - `OpenContain::crc()`

### xfer
- Purpose: Implements Xfer method for data serialization.
- Calls: 
  - `xfer->xferVersion()`
  - `OpenContain::xfer()`

### loadPostProcess
- Purpose: Handles post-load processing.
- Calls: 
  - `OpenContain::loadPostProcess()`

## Globals
None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/ThingTemplate.h"
  - "Common/Xfer.h"
  - "GameClient/InGameUI.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/AIUpdate.h"
  - "GameLogic/Module/POWTruckAIUpdate.h"
  - "GameLogic/Module/POWTruckBehavior.h"
