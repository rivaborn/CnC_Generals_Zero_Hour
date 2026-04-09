# GeneralsMD/Code/GameEngine/Source/GameLogic/ScriptEngine/ScriptConditions.cpp

## Purpose
Implements script condition evaluation for the game's scripting system, checking various game state conditions.

## Responsibilities
- Evaluates script conditions (e.g., unit destruction, player states, area triggers)
- Manages player/team lookups from script parameters
- Handles special skirmish-mode conditions
- Tracks transport statuses for units
- Integrates with audio, terrain, and UI systems for condition checks

## Key Types
- **ObjectTypesTemp (Class)**: Temporary wrapper for ObjectTypes instances
- **TransportStatus (Class)**: Tracks transport unit status (units, frame number)
- **TransportStatusMagicEnum (Enum)**: Not inferable (likely internal memory pool enum)
- **TransportStatus_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### evaluateCondition
- Purpose: Main dispatcher for all script condition evaluations
- Calls: All evaluate* functions (e.g., evaluateAllDestroyed, evaluateNamedUnitDestroyed)

### playerFromParam
- Purpose: Resolves player from script parameter (name or mask)
- Calls: ThePlayerList->getPlayerFromMask, TheScriptEngine->getPlayerFromAsciiString

### evaluateAllDestroyed
- Purpose: Checks if a player has no remaining objects
- Calls: Player->hasAnyObjects

### evaluateSkirmishPlayerHasDiscoveredPlayer
- Purpose: Checks if a skirmish player has discovered another player
- Calls: Object->getShroudedStatus

### evaluateMusicHasCompleted
- Purpose: Checks if a music track has completed playing
- Calls: TheAudio->hasMusicTrackCompleted

### evaluatePlayerLostObjectType
- Purpose: Checks if a player lost a specific object type
- Calls: Player->countObjectsByThingTemplate, TheScriptEngine->getObjectCount

## Globals
- **TheScriptConditions (ScriptConditionsInterface*)**: Global interface instance
- **s_transportStatuses (TransportStatus*)**: Tracks transport unit statuses

## Dependencies
- Common: GameEngine, MapObject, PlayerList, Player, SpecialPower, ThingTemplate, ThingFactory, Team, ObjectStatusTypes
- GameClient: ControlBar, Drawable, GameClient, InGameUI, View
- GameLogic: GameLogic, Module classes (AIUpdate, BodyModule, etc.), Object, ObjectTypes, PartitionManager, PolygonTrigger, ScriptConditions, ScriptEngine, Scripts, VictoryConditions
- Memory management: MemoryPoolObject, MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE
