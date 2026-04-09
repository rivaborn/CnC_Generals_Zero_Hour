# Generals/Code/GameEngine/Source/GameLogic/Object/Update/UpdateModule.cpp

## Purpose
This file contains the implementation of the `UpdateModule` class, which is responsible for managing the update scheduling and execution of game objects.

## Responsibilities
- Manages the sleep state and wake-up timing of game objects.
- Handles serialization (Xfer) for saving and loading game states.
- Ensures compatibility with old save files by adjusting module behavior.

## Key Types
- `UpdateModule` (Class): Base class for modules that need to be updated periodically.
- `UnsignedInt` (Typedef): Unsigned integer type used for frame counting.
- `UpdateSleepTime` (Typedef): Type representing sleep time for update scheduling.

## Key Functions
### frameToSleepTime
- Purpose: Calculates the sleep time based on given frames.
- Calls: `TheGameLogic->getFrame()`

### getWakeFrame
- Purpose: Determines the next wake-up frame for the module.
- Calls: `TheGameLogic->getFrame()`

### setWakeFrame
- Purpose: Sets the wake-up frame for a specific object.
- Calls: `TheGameLogic->friend_awakenUpdateModule()`

### crc
- Purpose: Computes the CRC for the module.
- Calls: `BehaviorModule::crc()`

### xfer
- Purpose: Handles serialization of the module.
- Calls: `xfer->xferVersion()`, `BehaviorModule::xfer()`, `xfer->xferUnsignedInt()`

### loadPostProcess
- Purpose: Performs post-processing after loading a game state.
- Calls: `BehaviorModule::loadPostProcess()`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/Xfer.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Module/UpdateModule.h"

- External symbols used but not defined here:
  - `TheGameLogic`
  - `BehaviorModule`
  - `Xfer`
