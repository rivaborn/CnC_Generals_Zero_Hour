# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/UpdateModule.cpp

## Purpose
Base class for update modules in the game logic system, handling timing and scheduling of updates.

## Responsibilities
- Manage update timing and scheduling for game objects
- Provide sleep/wake mechanisms for efficient updates
- Handle serialization (Xfer) for save/load functionality
- Support frame-based timing calculations

## Key Types
- `UpdateSleepTime` (Type): Represents sleep duration for updates
- `UpdateModule` (Class): Base class for update modules

## Key Functions
### `frameToSleepTime`
- Purpose: Calculate sleep time until a target frame
- Calls: `TheGameLogic->getFrame()`

### `getWakeFrame`
- Purpose: Get the frame when this module should wake
- Calls: `TheGameLogic->getFrame()`

### `setWakeFrame`
- Purpose: Schedule a wake-up call for this module
- Calls: `TheGameLogic->friend_awakenUpdateModule()`

### `crc`
- Purpose: Generate CRC checksum for serialization
- Calls: `BehaviorModule::crc()`

### `xfer`
- Purpose: Handle serialization/deserialization
- Calls: `BehaviorModule::xfer()`, `friend_setNextCallFrame()`

### `loadPostProcess`
- Purpose: Post-processing after loading
- Calls: `BehaviorModule::loadPostProcess()`

## Globals
- `TheGameLogic` (GameLogic*): Global game logic instance

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameLogic/GameLogic.h`, `GameLogic/Module/UpdateModule.h`
- `BehaviorModule` class
- `Xfer` class for serialization
- `Object` class for game objects
