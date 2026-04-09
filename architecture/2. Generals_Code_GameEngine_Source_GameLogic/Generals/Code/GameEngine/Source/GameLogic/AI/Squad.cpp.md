# Generals/Code/GameEngine/Source/GameLogic/AI/Squad.cpp

## Purpose
This file contains the implementation for managing squads in the game, including adding and removing objects, checking squad membership, and handling serialization.

## Responsibilities
- Manage a collection of object IDs representing squad members.
- Provide methods to add/remove objects from the squad.
- Retrieve all or live objects within the squad.
- Check if an object is part of the squad.
- Serialize/deserialize squad data for saving/loading game states.

## Key Types
- `Squad` (Class): Manages a group of game objects as a squad.

## Key Functions
### addObject
- Purpose: Adds an object to the squad by its ID.
- Calls: None

### removeObject
- Purpose: Removes an object from the squad by its ID.
- Calls: `std::find`, `m_objectIDs.erase`

### clearSquad
- Purpose: Clears all objects from the squad.
- Calls: `m_objectIDs.clear`, `m_objectsCached.clear`

### getAllObjects
- Purpose: Retrieves all objects in the squad, pruning dead ones.
- Calls: `TheGameLogic->findObjectByID`, `m_objectsCached.push_back`, `m_objectIDs.erase`

### getLiveObjects
- Purpose: Retrieves live (selectable) objects in the squad.
- Calls: `getAllObjects`, `m_objectsCached.erase`

### getSizeOfGroup
- Purpose: Returns the number of objects in the squad.
- Calls: None

### isOnSquad
- Purpose: Checks if an object is part of the squad.
- Calls: None

### squadFromTeam
- Purpose: Populates the squad with objects from a team.
- Calls: `fromTeam->iterate_TeamMemberList`, `m_objectIDs.push_back`

### squadFromAIGroup
- Purpose: Populates the squad with objects from an AI group.
- Calls: `fromAIGroup->getAllIDs`

### aiGroupFromSquad
- Purpose: Populates an AI group with live objects from the squad.
- Calls: `getLiveObjects`, `aiGroupToFill->add`

### crc
- Purpose: Handles CRC operations (currently empty).
- Calls: None

### xfer
- Purpose: Serializes/deserializes squad data.
- Calls: `xfer->xferVersion`, `xfer->xferUnsignedShort`, `xfer->xferObjectID`

## Globals
- None

## Dependencies
- Key includes:
  - "GameLogic/Squad.h"
  - "Common/GameState.h"
  - "Common/Team.h"
  - "Common/Xfer.h"
  - "GameLogic/AI.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
