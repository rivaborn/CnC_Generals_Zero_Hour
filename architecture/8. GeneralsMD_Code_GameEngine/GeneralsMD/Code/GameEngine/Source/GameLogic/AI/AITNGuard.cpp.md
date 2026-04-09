# GeneralsMD/Code/GameEngine/Source/GameLogic/AI/AITNGuard.cpp

## Purpose
Implements AI tunnel network guard behavior for units in Command & Conquer Generals Zero Hour.

## Responsibilities
- Manages state machine for tunnel network guard units
- Handles target selection and attack logic for tunnel defense
- Implements tunnel entry/exit behavior
- Processes crate pickup for guard units
- Tracks and responds to aggressors attacking tunnels

## Key Types
- AITNGuardMachine (Class): Main state machine for tunnel guard AI
- TunnelNetworkExitConditions (Class): Exit condition logic for guard states
- AITNGuardInnerState (Class): State for inner tunnel defense
- AITNGuardOuterState (Class): State for outer tunnel defense
- AITNGuardIdleState (Class): State for idle guard behavior

## Key Functions
### hasAttackedMeAndICanReturnFire
- Purpose: Checks if unit was attacked and can retaliate
- Calls: getMachineOwner, getBodyModule, getClearableLastAttacker, clearLastAttacker, findObjectByID, getRelationship, isEffectivelyDead, getAbleToAttackSpecificObject

### findBestTunnel
- Purpose: Finds closest tunnel to a given position
- Calls: getTunnelSystem, getContainerList, findObjectByID

### TunnelNetworkScan
- Purpose: Scans for enemy targets within guard vision range
- Calls: getClosestObject

## Globals
- CLOSE_ENOUGH (Real): Distance threshold constant

## Dependencies
- Common/PerfTimer.h
- Common/Team.h
- Common/Player.h
- Common/Xfer.h
- GameLogic/AI.h
- GameLogic/AIPathfind.h
- GameLogic/AITNGuard.h
- GameLogic/Module/AIUpdate.h
- GameLogic/Module/BodyModule.h
- GameLogic/Module/CollideModule.h
- Common/TunnelTracker.h
- GameLogic/Object.h
- GameLogic/PartitionManager.h
- GameLogic/PolygonTrigger.h
