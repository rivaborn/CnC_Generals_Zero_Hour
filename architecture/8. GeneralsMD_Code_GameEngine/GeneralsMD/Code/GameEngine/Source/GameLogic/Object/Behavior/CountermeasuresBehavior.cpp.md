# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/CountermeasuresBehavior.cpp

## Purpose
Handles countermeasure firing when under missile threat and diverts missiles to flares.

## Responsibilities
- Tracks incoming missiles and calculates evasion
- Launches countermeasure volleys (flares) at calculated intervals
- Manages countermeasure reload cycles
- Validates and cleans up active flares
- Determines closest flare for missile diversion

## Key Types
- **CountermeasuresPlayerScanHelper (Struct)**: Helper struct for scanning objects (contains kind mask, healer object, and object list)
- **CountermeasuresBehavior (Class)**: Main behavior class managing countermeasures

## Key Functions
### checkForCountermeasures
- Purpose: Scans for objects matching criteria (player, kind, health) and adds them to a list
- Calls: `testObj->isEffectivelyDead()`, `testObj->getControllingPlayer()`, `testObj->isOffMap()`, `testObj->isAnyKindOf()`, `testObj->getBodyModule()->getHealth()`, `testObj->getBodyModule()->getMaxHealth()`

### reportMissileForCountermeasures
- Purpose: Records incoming missiles and determines if they should be diverted
- Calls: `TheGameLogic->getFrame()`, `GameLogicRandomValueReal()`, `pui->setFramesTillCountermeasureDiversionOccurs()`

### calculateCountermeasureToDivertTo
- Purpose: Finds the closest active flare for missile diversion
- Calls: `TheGameLogic->findObjectByID()`, `ThePartitionManager->getDistanceSquared()`

### update
- Purpose: Main update loop handling volley launching, reloading, and flare validation
- Calls: `TheGameLogic->getFrame()`, `TheGameLogic->findObjectByID()`, `launchVolley()`, `reloadCountermeasures()`

### launchVolley
- Purpose: Creates and launches a volley of flares with calculated trajectories
- Calls: `TheThingFactory->findTemplate()`, `TheThingFactory->newObject()`, `obj->getUnitDirectionVector3D()`, `physics->transferVelocityTo()`, `flare->getPhysics()->applyMotiveForce()`

## Globals
- None

## Dependencies
- Key includes: `PreRTS.h`, `Common/Thing.h`, `Common/ThingTemplate.h`, `Common/INI.h`, `Common/Player.h`, `Common/ThingFactory.h`, `Common/Xfer.h`, `GameClient/ParticleSys.h`, `GameClient/Anim2D.h`, `GameClient/InGameUI.h`, `GameLogic/Module/CountermeasuresBehavior.h`, `GameLogic/Module/BodyModule.h`, `GameLogic/Module/PhysicsUpdate.h`, `GameLogic/GameLogic.h`, `GameLogic
