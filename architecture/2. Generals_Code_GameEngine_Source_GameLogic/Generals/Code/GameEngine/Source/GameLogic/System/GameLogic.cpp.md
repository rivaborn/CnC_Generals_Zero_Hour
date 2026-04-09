# Generals/Code/GameEngine/Source/GameLogic/System/GameLogic.cpp

## Purpose
This file contains the implementation of the `GameLogic` class, which manages game state, object creation, destruction, and updates in Command & Conquer Generals.

## Responsibilities
- Manages game initialization and shutdown.
- Handles object creation, destruction, and updating.
- Manages game logic such as AI, scripting, and terrain.
- Coordinates loading and saving of game states.

## Key Types
- `GameLogic` (Class): Main class managing game state and logic.
- Various enums for load progress stages.

## Key Functions
### GameLogic::init
- Purpose: Initializes the game logic system.
- Calls: 
  - `setFPMode`
  - `setDefaults`
  - Creates various managers like `PartitionManager`, `TerrainLogic`, etc.

### GameLogic::destroyAllObjectsImmediate
- Purpose: Destroys all objects in the game immediately.
- Calls:
  - `destroyObject`
  - `processDestroyList`

### GameLogic::xfer
- Purpose: Handles serialization and deserialization of game logic state.
- Calls:
  - Various xfer functions for different components like terrain, scripts, etc.

## Globals
- `TheGameLogic` (GameLogic*): Singleton instance of the game logic.
- `inCRCGen` (Not inferable): Possibly related to CRC generation.

## Dependencies
- Includes headers from various modules such as AI, scripting, networking, and UI components.
