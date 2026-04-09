# Generals/Code/GameEngine/Source/GameLogic/Object/Create/PreorderCreate.cpp

## Purpose
This file contains the implementation of the `PreorderCreate` class, which handles preorder status for buildings in Command & Conquer Generals.

## Responsibilities
- Manage preorder status for created objects.
- Set or clear model condition states based on preorder status.
- Implement CRC and Xfer methods for serialization.

## Key Types
- PreorderCreate (Class): Manages preorder status for game objects.

## Key Functions
### onCreate
- Purpose: Handles the creation of an object.
- Calls: None

### onBuildComplete
- Purpose: Sets or clears the preorder model condition state based on player's preorder status.
- Calls: 
  - `getObject()->getControllingPlayer()->didPlayerPreorder()`
  - `getObject()->setModelConditionState( MODELCONDITION_PREORDER )`
  - `getObject()->clearModelConditionState( MODELCONDITION_PREORDER )`

### crc
- Purpose: Implements CRC method for serialization.
- Calls: `CreateModule::crc( xfer )`

### xfer
- Purpose: Implements Xfer method for serialization.
- Calls: 
  - `xfer->xferVersion( &version, currentVersion )`
  - `CreateModule::xfer( xfer )`

### loadPostProcess
- Purpose: Handles post-processing after loading.
- Calls: `CreateModule::loadPostProcess()`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/Player.h"
  - "Common/Xfer.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/PreorderCreate.h"
