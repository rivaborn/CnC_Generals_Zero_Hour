# Generals/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/WanderAIUpdate.cpp

## Purpose
This file implements the `WanderAIUpdate` class, which provides random movement commands to AI-controlled objects in the game.

## Responsibilities
- Creates and manages an AI state machine for wandering behavior.
- Updates the object's position randomly if it is idle.
- Handles CRC (Cyclic Redundancy Check) and Xfer (transfer) operations for saving/loading the object's state.

## Key Types
- `WanderAIUpdate` (Class): Manages random movement for AI objects.
- None

## Key Functions
### makeStateMachine
- Purpose: Creates a new AI state machine instance.
- Calls: `newInstance(AIStateMachine)`

### WanderAIUpdate Constructor
- Purpose: Initializes the `WanderAIUpdate` object.
- Calls: None

### WanderAIUpdate Destructor
- Purpose: Cleans up resources for the `WanderAIUpdate` object.
- Calls: None

### update
- Purpose: Updates the AI's position randomly if it is idle.
- Calls: `isIdle`, `aiMoveToPosition`

### crc
- Purpose: Handles CRC operations for the object.
- Calls: `AIUpdateInterface::crc`

### xfer
- Purpose: Handles Xfer operations for saving/loading the object's state.
- Calls: `xfer->xferVersion`, `AIUpdateInterface::xfer`

### loadPostProcess
- Purpose: Performs post-processing after loading the object's state.
- Calls: `AIUpdateInterface::loadPostProcess`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/RandomValue.h"
  - "GameLogic/Module/WanderAIUpdate.h"
  - "GameLogic/Object.h"

- External symbols used but not defined here:
  - `AIStateMachine`
  - `Thing
