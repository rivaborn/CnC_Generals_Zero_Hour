# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/RebuildHoleBehavior.cpp

## Purpose
Implements behavior for GLA "hole" objects that reconstruct buildings after destruction.

## Responsibilities
- Manages worker spawning and reconstruction process
- Handles health regeneration for holes
- Transfers attackers and sticky bombs to new buildings
- Cleans up worker and hole when reconstruction completes

## Key Types
- **RebuildHoleBehaviorModuleData (struct)**: Configuration data for hole behavior
- **RebuildHoleBehavior (class)**: Main behavior module handling reconstruction logic
- **RebuildHoleBehaviorInterface (interface)**: Access to hole behavior functionality

## Key Functions
### newWorkerRespawnProcess
- Purpose: Spawns or respawns worker units for reconstruction
- Calls: TheGameLogic->destroyObject, getObject()->maskObject

### startRebuildProcess
- Purpose: Initiates the building reconstruction process
- Calls: newWorkerRespawnProcess

### update
- Purpose: Main update loop handling worker spawning, health regeneration, and reconstruction completion
- Calls: TheGameLogic->findObjectByID, TheThingFactory->newObject, TheGameLogic->destroyObject, body->attemptHealing

### onDie
- Purpose: Cleanup when hole is destroyed
- Calls: TheGameLogic->destroyObject

### xfer
- Purpose: Serialization for network/savegame support
- Calls: UpdateModule::xfer, TheThingFactory->findTemplate

## Globals
- None

## Dependencies
- Common/GameState.h
- Common/ThingFactory.h
- GameLogic/GameLogic.h
- GameLogic/Module/RebuildHoleBehavior.h
- GameLogic/Module/StickyBombUpdate.h
- GameClient/Drawable.h
- GameLogic/ScriptEngine.h
