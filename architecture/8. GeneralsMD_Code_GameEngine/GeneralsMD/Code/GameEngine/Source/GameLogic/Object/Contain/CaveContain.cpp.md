# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Contain/CaveContain.cpp

## Purpose
Manages cave containment logic for objects in the game, extending OpenContain to handle cave-specific behavior.

## Responsibilities
- Manages objects contained within cave systems
- Handles team changes when objects enter/leave caves
- Coordinates with TunnelTracker for cave operations
- Manages cave registration and deregistration
- Handles cave team synchronization across connected caves

## Key Types
- **CaveContain (Class)**: Main class handling cave containment logic
- **TunnelTracker (External)**: Tracks cave connections and contents
- **CaveInterface (Interface)**: Provides cave-related functionality

## Key Functions
### findCave
- Purpose: Finds the CaveInterface module for a given object
- Calls: None (iterates behavior modules)

### CaveContain::onDie
- Purpose: Handles cave destruction and cleanup
- Calls: TheCaveSystem->unregisterCave, myTracker->onTunnelDestroyed

### CaveContain::onBuildComplete
- Purpose: Registers new cave when construction completes
- Calls: TheCaveSystem->registerNewCave, myTracker->onTunnelCreated

### CaveContain::changeTeamOnAllConnectedCaves
- Purpose: Synchronizes team changes across connected caves
- Calls: TheGameLogic->findObjectByID, currentCave->defect

## Globals
- **TheCaveSystem (External)**: Global cave system manager
- **ThePartitionManager (External)**: Global partition manager
- **ThePlayerList (External)**: Global player list
- **TheGlobalData (External)**: Global game data
- **TheTeamFactory (External)**: Team factory instance

## Dependencies
- Common/GameState.h
- Common/Player.h
- Common/PlayerList.h
- Common/Team.h
- Common/ThingTemplate.h
- Common/TunnelTracker.h
- Common/Xfer.h
- GameClient/Drawable.h
- GameLogic/Module/AIUpdate.h
- GameLogic/Module/CaveContain.h
- GameLogic/CaveSystem.h
- GameLogic/Object.h
- GameLogic/PartitionManager.h
