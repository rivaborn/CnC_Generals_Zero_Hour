# GeneralsMD/Code/GameEngine/Source/GameLogic/AI/AISkirmishPlayer.cpp

## Purpose
Implements the AI logic for skirmish (single-player) game mode, controlling computer opponents.

## Responsibilities
- Manages base construction and defense
- Handles unit production and team building
- Controls superweapon targeting
- Adjusts build lists based on starting position
- Manages dozer (construction unit) allocation

## Key Types
- **AISkirmishPlayer (Class)**: Main AI player class for skirmish mode
- **TeamInQueue (Struct)**: Tracks queued team builds
- **AISideBuildList (Struct)**: Contains side-specific build lists

## Key Functions
### processBaseBuilding
- Purpose: Builds and maintains base structures
- Calls: TheThingFactory->findTemplate, TheGameLogic->findObjectByID, TheBuildAssistant->canMakeUnit

### processTeamBuilding
- Purpose: Manages unit team production
- Calls: selectTeamToBuild, queueUnits

### computeSuperweaponTarget
- Purpose: Determines optimal superweapon targeting
- Calls: getPlayerStructureBounds, TheTerrainLogic->getClosestWaypointOnPath

### adjustBuildList
- Purpose: Rotates build positions based on starting location
- Calls: TheTerrainLogic->getMaximumPathfindExtent

### newMap
- Purpose: Initializes AI for new maps
- Calls: TheAI->getAiData()->m_sideBuildLists, buildStructureNow

## Globals
- **USE_DOZER (Define)**: Controls dozer construction system
- **TheAI (Global)**: Access to AI system
- **TheGameLogic (Global)**: Game logic interface
- **TheThingFactory (Global)**: Thing template factory
- **TheBuildAssistant (Global)**: Build assistance system
- **TheScriptEngine (Global)**: Script execution engine

## Dependencies
- Common/GameMemory.h
- Common/Player.h
- GameLogic/AI.h
- GameLogic/AIPathfind.h
- GameLogic/Module/ProductionUpdate.h
- GameClient/TerrainVisual.h
- PreRTS.h (must be first include)
