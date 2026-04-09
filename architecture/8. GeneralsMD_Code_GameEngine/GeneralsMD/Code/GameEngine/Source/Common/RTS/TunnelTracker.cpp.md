# GeneralsMD/Code/GameEngine/Source/Common/RTS/TunnelTracker.cpp

## Purpose
Manages tunnel systems in the game, tracking contained objects and tunnel state.

## Responsibilities
- Tracks tunnels and objects contained within them
- Manages tunnel capacity and healing of contained objects
- Handles tunnel creation/destruction events
- Maintains a "nemesis" target system for tunnels

## Key Types
- TunnelTracker (Class): Main class managing tunnel systems
- ContainIterateFunc (Type): Function pointer type for iterating contained objects

## Key Functions
### iterateContained
- Purpose: Iterates through contained objects with a callback function
- Calls: None (uses STL iterators)

### updateNemesis
- Purpose: Updates the current nemesis target for tunnels
- Calls: TheGameLogic->getFrame()

### getCurNemesis
- Purpose: Retrieves the current nemesis target if valid
- Calls: TheGameLogic->findObjectByID(), TheGameLogic->getFrame()

### onTunnelDestroyed
- Purpose: Handles tunnel destruction events
- Calls: TheGameLogic->findObjectByID(), iterateContained()

### healObjects
- Purpose: Heals all objects within tunnels
- Calls: iterateContained()

### xfer
- Purpose: Serializes tunnel tracker state
- Calls: Xfer methods (xferVersion, xferSTLObjectIDList, etc.)

## Globals
- None

## Dependencies
- Common/GameState.h
- Common/GlobalData.h
- Common/KindOf.h
- Common/TunnelTracker.h
- Common/Xfer.h
- GameClient/ControlBar.h
- GameClient/Drawable.h
- GameLogic/AI.h
- GameLogic/AIPathfind.h
- GameLogic/GameLogic.h
- GameLogic/Object.h
- GameLogic/PartitionManager.h
- GameLogic/Module/BodyModule.h
- GameLogic/Module/TunnelContain.h
