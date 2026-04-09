# GeneralsMD/Code/GameEngine/Include/GameLogic/GameLogic.h

## Purpose
Header defining the GameLogic singleton class, core game state manager for C&C Generals.

## Responsibilities
- Manages game objects, updates, and state
- Handles game mode transitions and loading
- Provides object lookup and ID management
- Controls game pausing and scoring
- Manages sleepy/non-sleepy update modules

## Key Types
- **GameLogic (Class)**: Core game state manager
- **BuildableMap (Class)**: Maps templates to buildable status overrides
- **ControlBarOverrideMap (Class)**: Maps command sets to button overrides
- **ObjectTOCEntry (Struct)**: Table of contents entry for object serialization
- **BuildableStatus (Enum)**: Buildable status flags
- **GameLogicFuncPtr (Type)**: Function pointer for game logic callbacks

## Key Functions
### `processCommandList`
- Purpose: Process a command list
- Calls: Not inferable

### `registerObject`
- Purpose: Register an object with GameLogic
- Calls: Not inferable

### `destroyObject`
- Purpose: Mark object for destruction
- Calls: Not inferable

### `update`
- Purpose: Update game state
- Calls: `processDestroyList`, `remakeSleepyUpdate`

## Globals
- **TheGameLogic (GameLogic*)**: Singleton instance

## Dependencies
- Common/GameCommon.h, GameType.h, Snapshot.h
- GameNetwork/NetworkDefs.h
- GameLogic/Module/UpdateModule.h
- STL containers (vector, map, list)
