# GeneralsMD/Code/GameEngine/Source/Common/RTS/Team.cpp

## Purpose
Implements team management functionality for the game, including team creation, relations, and member operations.

## Responsibilities
- Manages team prototypes and instances
- Handles team relations and player relations
- Provides team member operations (recruitment, evacuation, killing)
- Serializes team state for save/load
- Executes team-specific scripts

## Key Types
- TeamFactory (Class): Manages creation and lookup of teams
- TeamPrototype (Class): Template for creating teams
- Team (Class): Represents a team of game objects
- TeamRelationMap (Class): Stores relationships between teams
- Relationship (Enum): Defines team relationship types (ally, enemy, neutral)

## Key Functions
### locoSetMatches
- Purpose: Checks if locomotor surface type matches given bit flags
- Calls: None

### deleteTeamCallback
- Purpose: Callback for deleting team instances
- Calls: Not inferable from snippet

### isInBuildVariations
- Purpose: Checks if an object is in build variations
- Calls: Not inferable from snippet

### TeamFactory::createInactiveTeam
- Purpose: Creates a team that's not yet active
- Calls: TeamPrototype::getFirstItemIn_TeamInstanceList, ScriptEngine::findScriptByName, ScriptEngine::friend_executeAction

### Team::recruitClosestUnit
- Purpose: Finds the closest recruitable unit for the team
- Calls: Object::getAIUpdateInterface, AIUpdateInterface::isRecruitable, Object::isDisabledByType

### Team::killTeam
- Purpose: Destroys all team members
- Calls: Team::evacuateTeam, Object::kill, PlayerList::getNeutralPlayer

## Globals
- TheTeamFactory (TeamFactory*): Global instance of the team factory

## Dependencies
- Common/GameState.h
- Common/Team.h
- Common/ThingFactory.h
- Common/PerfTimer.h
- Common/Player.h
- Common/PlayerList.h
- Common/PlayerTemplate.h
- Common/ThingTemplate.h
- Common/WellKnownKeys.h
- Common/Xfer.h
- GameClient/Drawable.h
- GameLogic/SidesList.h
- GameLogic/Object.h
- GameLogic/Module/BodyModule.h
- GameLogic/Module/ContainModule.h
- GameLogic/Module/AIUpdate.h
- GameLogic/PolygonTrigger.h
- GameLogic/Module/AIUpdate.h
- GameLogic/PartitionManager.h
- GameLogic/ScriptActions.h
- GameLogic/ScriptEngine.h
