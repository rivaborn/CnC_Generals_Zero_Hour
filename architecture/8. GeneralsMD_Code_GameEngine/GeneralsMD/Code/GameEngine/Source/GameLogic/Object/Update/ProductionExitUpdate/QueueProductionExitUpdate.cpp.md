# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/ProductionExitUpdate/QueueProductionExitUpdate.cpp

## Purpose
Manages the queued exit of produced units from buildings, handling positioning, delays, and rally points.

## Responsibilities
- Spawns units at correct exit positions with proper orientation
- Enforces production delays and burst counts
- Calculates rally points and paths for exiting units
- Handles physics for airborne unit creation
- Manages door reservation for exit sequencing

## Key Types
- **QueueProductionExitUpdate (Class)**: Module handling queued unit production exits
- **QueueProductionExitUpdateModuleData (Struct)**: Configuration data for exit behavior
- **ExitDoorType (Enum)**: Exit door identifiers (DOOR_1, DOOR_NONE_AVAILABLE)

## Key Functions
### exitObjectViaDoor
- Purpose: Spawns a unit through a building exit door with proper positioning and physics
- Calls: getObject, getQueueProductionExitUpdateModuleData, getTransformMatrix, getGroundHeight, getPhysics, applyMotiveForce, setPitchRate, addObjectToPathfindMap, snapPosition, adjustDestination, aiFollowExitProductionPath

### exitObjectByBudding
- Purpose: Handles unit creation via budding (spawning from host object)
- Calls: getPosition, getOrientation, getLayer, setPosition, setOrientation, setLayer, aiMoveToPosition, getQueueProductionExitUpdateModuleData

### update
- Purpose: Manages production delay timing and burst count
- Calls: isFreeToExit

### getNaturalRallyPoint
- Purpose: Calculates the natural rally point for exiting units
- Calls: getQueueProductionExitUpdateModuleData, getTransformMatrix

## Globals
- **TheAI (AI**) : Global AI instance for pathfinding
- **TheTerrainLogic (TerrainLogic**) : Global terrain system for height queries

## Dependencies
- Common/RandomValue.h, Common/ThingTemplate.h, Common/Xfer.h
- Lib/BaseType.h
- GameLogic/AI.h, GameLogic/AIPathfind.h, GameLogic/Object.h
- GameLogic/Module/AIUpdate.h, GameLogic/Module/PhysicsUpdate.h, GameLogic/Module/QueueProductionExitUpdate.h
