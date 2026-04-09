# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate.cpp

## Purpose
Implements generic AI mechanisms for game objects, including pathfinding, state management, and command processing.

## Responsibilities
- Manages AI state machines and behaviors
- Handles pathfinding and movement logic
- Processes player and AI commands
- Manages locomotor selection and turret behavior
- Serializes AI state for save/load

## Key Types
- `AIUpdateModuleData` (Class): Stores AI configuration and turret data
- `AIUpdateInterface` (Class): Core AI update interface for game objects
- `WAYPOINT_PATH_LIMIT` (Enum): Defines waypoint path limits

## Key Functions
### `AIUpdateInterface::makeStateMachine`
- Purpose: Creates a new AI state machine instance
- Calls: `newInstance(AIStateMachine)`

### `AIUpdateInterface::setGoalPositionClipped`
- Purpose: Sets the AI's goal position with boundary checks
- Calls: `TheTerrainLogic->getExtent`, `getStateMachine()->setGoalPosition`

### `AIUpdateInterface::crc`
- Purpose: Generates CRC checksum for serialization
- Calls: `UpdateModule::crc`, `xfer`

### `AIUpdateInterface::xfer`
- Purpose: Serializes/deserializes AI state
- Calls: `UpdateModule::xfer`, various xfer methods

## Globals
- `TheLocomotorSetNames` (Array): Locomotor set name definitions
- `TheAutoAcquireEnemiesNames` (Array): Auto-acquire enemy name definitions

## Dependencies
- Common: `ActionManager.h`, `GameState.h`, `Player.h`, etc.
- GameLogic: `AI.h`, `Locomotor.h`, `Object.h`, etc.
- GameClient: `ControlBar.h`, `Drawable.h`, etc.
- External: `TheGlobalData`, `TheTerrainLogic`, `TheAI`, `TheScriptEngine`
