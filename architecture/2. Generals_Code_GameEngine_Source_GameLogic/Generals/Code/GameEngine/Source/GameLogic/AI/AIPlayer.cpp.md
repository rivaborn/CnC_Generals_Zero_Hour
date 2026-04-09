# Generals/Code/GameEngine/Source/GameLogic/AI/AIPlayer.cpp

## Purpose
This file contains the implementation for `AIPlayer`, which manages AI behavior in Command & Conquer Generals, including building structures, managing teams, and handling supply logistics.

## Responsibilities
- Manage AI player's structure and unit production.
- Handle supply center operations and resource gathering.
- Queue and manage teams of units.
- Process events related to built structures and units.

## Key Types
- `AIPlayer` (Class): Manages AI player behavior.
- `TeamInQueue` (Class): Represents a queue for building teams.
- `WorkOrder` (Class): Represents an order to build a specific unit or structure.

## Key Functions
### onStructureProduced
- Purpose: Handles actions when a structure is finished building.
- Calls: 
  - `updateObjValuesFromMapProperties`
  - `clearStatus`
  - `runObjectScript`
  - `checkForSupplyCenter`

### checkForSupplyCenter
- Purpose: Determines if a built structure is a supply center and sets up resource gathering.
- Calls: 
  - `findUpdateModule`
  - `getGlobalDifficulty`
  - `setDesiredGatherers`

### queueSupplyTruck
- Purpose: Queues a supply truck to be built if needed.
- Calls: 
  - `iterate_TeamBuildQueue`
  - `iterate_TeamInstanceList`
  - `iterate_TeamMemberList`
  - `findFactory`
  - `newInstance(WorkOrder)`

## Globals
- None

## Dependencies
- Key includes:
  - "Common/GameMemory.h"
  - "Common/GameState.h"
  - "GameLogic/AIPlayer.h"
  - "GameLogic/Team.h"
  - "GameLogic/Object.h"
  - "GameLogic/SidesList.h"
  - "GameLogic/ScriptEngine.h"
  - "GameLogic/PartitionManager.h"
