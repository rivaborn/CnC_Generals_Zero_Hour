# Generals/Code/GameEngine/Source/GameLogic/Object/Helper/ObjectHelper.cpp

## Purpose
This file contains the implementation of the `ObjectHelper` class, which provides helper functions for game objects in Command & Conquer Generals.

## Responsibilities
- Manage object sleep states.
- Handle CRC (Cyclic Redundancy Check) calculations.
- Implement Xfer methods for data transfer.
- Perform post-load processing.

## Key Types
- ObjectHelper (Class): Provides helper functions for game objects.

## Key Functions
### ~ObjectHelper
- Purpose: Destructor for the `ObjectHelper` class.
- Calls: None

### sleepUntil
- Purpose: Sets the object to sleep until a specified frame.
- Calls: 
  - getObject()->getStatusBits()
  - setWakeFrame()

### crc
- Purpose: Updates the CRC for the module.
- Calls: UpdateModule::crc()

### xfer
- Purpose: Handles data transfer for the module.
- Calls: 
  - xfer->xferVersion()
  - UpdateModule::xfer()

### loadPostProcess
- Purpose: Performs post-load processing for the module.
- Calls: UpdateModule::loadPostProcess()

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/Xfer.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/ObjectHelper.h"
