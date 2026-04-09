# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/WanderAIUpdate.cpp

## Purpose
Implements the WanderAIUpdate module, which makes objects move randomly when idle.

## Responsibilities
- Creates an AI state machine for wandering behavior
- Generates random movement commands when the object is idle
- Handles serialization (Xfer) and CRC for network sync
- Extends AIUpdateInterface functionality

## Key Types
- **WanderAIUpdate (Class)**: AI module that triggers random movement for idle objects
- **AIStateMachine (Class)**: State machine for AI behavior (external)

## Key Functions
### `makeStateMachine`
- Purpose: Creates and returns a new AIStateMachine instance for wandering.
- Calls: `newInstance(AIStateMachine)`

### `update`
- Purpose: Updates the AI logic; issues random move commands if the object is idle.
- Calls: `isIdle()`, `getObject()`, `getPosition()`, `GameLogicRandomValue()`, `aiMoveToPosition()`, `AIUpdateInterface::update()`

### `crc`
- Purpose: Serializes/deserializes the object for network sync (CRC).
- Calls: `AIUpdateInterface::crc()`

### `xfer`
- Purpose: Handles versioned serialization of the module.
- Calls: `xfer->xferVersion()`, `AIUpdateInterface::xfer()`

### `loadPostProcess`
- Purpose: Post-processing after loading (currently just delegates to base).
- Calls: `AIUpdateInterface::loadPostProcess()`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/RandomValue.h`, `GameLogic/Module/WanderAIUpdate.h`, `GameLogic/Object.h`
- `AIStateMachine`, `AIUpdateInterface`, `Thing`, `Coord3D`, `Xfer`, `UpdateSleepTime`
