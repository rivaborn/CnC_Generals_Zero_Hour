# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/JetAIUpdate.cpp

## Purpose
Implements AI behavior for jets and helicopters, including takeoff, landing, taxiing, and parking logic.

## Responsibilities
- Manages jet/helicopter state machine transitions
- Handles runway clearance and parking space reservation
- Controls taxiing, takeoff, and landing sequences
- Manages special reload ammo behavior
- Handles afterburner effects and sounds

## Key Types
- **TaxiType (Enum)**: Taxi direction (FROM_HANGAR, FROM_PARKING, TO_PARKING)
- **JetAIStateType (Enum)**: AI state types (TAXI_FROM_HANGAR, TAKING_OFF, LANDING, etc.)
- **PartitionFilterHasParkingPlace (Class)**: Partition filter for objects with available parking
- **JetAwaitingRunwayState (Class)**: State for waiting for runway clearance
- **JetOrHeliCirclingDeadAirfieldState (Class)**: State for circling when airfield is dead
- **JetAIStateMachine (Class)**: State machine for jet AI behavior
- **HeliAIStateMachine (Class)**: State machine for helicopter AI behavior

## Key Functions
### getPP
- Purpose: Retrieves parking place behavior interface for an airfield
- Calls: TheGameLogic->findObjectByID, getBehaviorModules, getParkingPlaceBehaviorInterface

### findSuitableAirfield
- Purpose: Finds closest airfield with available parking space
- Calls: PartitionManager queries with various filters

### intersectInfiniteLine2D
- Purpose: Calculates intersection between two infinite lines in 2D
- Calls: None (math operations)

### calcDistSqr
- Purpose: Calculates squared distance between two 3D coordinates
- Calls: None (math operations)

## Globals
- **BIGNUM (Real)**: Large number constant (99999.0f)

## Dependencies
- Common/ActionManager.h
- Common/GlobalData.h
- Common/MiscAudio.h
- Common/ThingFactory.h
- Common/ThingTemplate.h
- GameClient/Drawable.h
- GameClient/GameClient.h
- GameLogic/ExperienceTracker.h
- GameLogic/Locomotor.h
- GameLogic/Module/BodyModule.h
- GameLogic/Module/CountermeasuresBehavior.h
- GameLogic/Module/JetAIUpdate.h
- GameLogic/Module/ParkingPlaceBehavior.h
- GameLogic/Module/PhysicsUpdate.h
- GameLogic/Object.h
- GameLogic/AIPathfind.h
- GameLogic/PartitionManager.h
- GameLogic/Weapon.h
