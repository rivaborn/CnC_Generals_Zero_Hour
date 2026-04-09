# Generals/Code/GameEngine/Source/GameLogic/AI/AISkirmishPlayer.cpp

## Purpose
This file implements the AI logic for a skirmish player in Command & Conquer Generals, handling base building, unit production, and team management.

## Responsibilities
- Manage base construction and defense.
- Handle unit production and team reinforcement.
- Adjust build list based on starting position.
- Compute superweapon targets.
- Implement CRC and Xfer methods for data serialization.

## Key Types
- **AISkirmishPlayer (Class)**: Manages AI logic for a skirmish player, including base building, unit production, and team management.

## Key Functions
### processBaseBuilding
- Purpose: Refreshes and rebuilds missing base buildings.
- Calls:
  - `TheGameLogic->findObjectByID`
  - `RebuildHoleBehavior::getRebuildHoleBehaviorInterfaceFromObject`
  - `TheBuildAssistant->canMakeUnit`
  - `buildStructureWithDozer` or `buildStructureNow`

### startTraining
- Purpose: Starts training a unit at a factory.
- Calls:
  - `findFactory`
  - `queueCreateUnit`

### isAGoodIdeaToBuildTeam
- Purpose: Checks if a team prototype can be built based on conditions and limits.
- Calls:
  - `evaluateProductionCondition`
  - `countTeamInstances`
  - `isPossibleToBuildTeam`

### doBaseBuilding
- Purpose: Determines when to start building another base structure.
- Calls:
  - `processBaseBuilding`

### processTeamBuilding
- Purpose: Selects and queues units for a new team.
- Calls:
  - `selectTeamToBuild`
  - `queueUnits`

### update
- Purpose: Main AI update function, calls other processing functions.

## Globals
- None

## Dependencies
- Key includes:
  - "Common/GameMemory.h"
  - "Common/GlobalData.h"
  - "Common/Player.h"
  - "GameLogic/AISkirmishPlayer.h"
  - "GameLogic/TerrainLogic.h"
  - "GameLogic/ScriptEngine.h"
