# Generals/Code/GameEngine/Source/Common/RTS/Team.cpp

## Purpose
This file implements the `Team` and related classes, managing teams of game objects in Command & Conquer Generals.

## Responsibilities
- Manages team creation, destruction, and membership.
- Handles team relationships and interactions.
- Implements serialization for saving/loading team states.
- Provides functions for team actions like evacuation and damage.

## Key Types
- `Team`: Represents a group of game objects with shared properties.
- `TeamFactory`: Manages the creation and lifecycle of teams.
- `TeamRelationMap`: Stores relationship data between teams.

## Key Functions
### locoSetMatches
- Purpose: Checks if locomotor surface type matches given bit flags.
- Calls: None

### deleteTeamCallback
- Purpose: Callback for deleting a team.
- Calls: None

### isInBuildVariations
- Purpose: Determines if an object is in build variations.
- Calls: None

## Globals
- `TheTeamFactory` (TeamFactory*): Global instance of the team factory.

## Dependencies
- Includes:
  - "PreRTS.h"
  - "Common/GameState.h"
  - "Common/Team.h"
  - "Common/ThingFactory.h"
  - "Common/PerfTimer.h"
  - "Common/Player.h"
  - "Common/PlayerList.h"
  - "Common/PlayerTemplate.h"
  - "Common/ThingTemplate.h"
  - "Common/WellKnownKeys.h"
  - "Common/Xfer.h"
  - "GameClient/Drawable.h"
  - "GameLogic/SidesList.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/BodyModule.h"
  - "GameLogic/Module/ContainModule.h"
  - "GameLogic/PolygonTrigger.h"
  - "GameLogic/Module/AIUpdate.h"
  - "GameLogic/PartitionManager.h"
  - "GameLogic/ScriptActions.h"
  - "GameLogic/ScriptEngine.h"
