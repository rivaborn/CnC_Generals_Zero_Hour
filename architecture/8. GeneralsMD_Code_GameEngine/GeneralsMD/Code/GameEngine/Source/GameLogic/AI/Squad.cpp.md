# GeneralsMD/Code/GameEngine/Source/GameLogic/AI/Squad.cpp

## Purpose
Manages groups of game objects (squads) for AI and team operations in Command & Conquer Generals.

## Responsibilities
- Maintains lists of object IDs in a squad
- Provides methods to add/remove objects and convert between squad/team/AIGroup formats
- Handles serialization (Xfer) for save/load functionality
- Caches live/selectable objects for efficient access

## Key Types
- `Squad` (Class): Manages a collection of game objects (squad)
- `VecObjectID` (Type): Vector of ObjectID representing squad members
- `VecObjectPtr` (Type): Vector of Object pointers for cached objects

## Key Functions
### `addObject`
- Purpose: Adds an object to the squad by its ID
- Calls: `getID()`

### `removeObject`
- Purpose: Removes an object from the squad
- Calls: `getID()`, `std::find`, `erase`

### `getAllObjects`
- Purpose: Returns all valid objects in the squad, pruning dead references
- Calls: `TheGameLogic->findObjectByID()`

### `getLiveObjects`
- Purpose: Returns only selectable (live) objects in the squad
- Calls: `getAllObjects()`, `isSelectable()`

### `squadFromTeam`
- Purpose: Converts a team into a squad
- Calls: `iterate_TeamMemberList()`, `getID()`

### `aiGroupFromSquad`
- Purpose: Converts a squad into an AIGroup
- Calls: `getLiveObjects()`, `AIGroup::add()`

### `xfer`
- Purpose: Serializes squad data for save/load
- Calls: `xferVersion`, `xferUnsignedShort`, `xferObjectID`

## Globals
- `TheGameLogic` (External): Access to game logic system

## Dependencies
- `Squad.h`, `GameState.h`, `Team.h`, `Xfer.h`, `AI.h`, `GameLogic.h`, `Object.h`
- Uses STL containers (`vector`, `find`, `erase`)
- Depends on `Xfer` class for serialization
- Uses `ObjectID` and `Object` types from game engine
