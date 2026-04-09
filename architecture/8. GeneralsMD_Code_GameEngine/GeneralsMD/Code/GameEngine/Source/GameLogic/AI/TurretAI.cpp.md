# GeneralsMD/Code/GameEngine/Source/GameLogic/AI/TurretAI.cpp

## Purpose
Implements turret behavior logic for the game, including aiming, firing, and idle states.

## Responsibilities
- Manages turret state machine transitions
- Handles turret rotation and pitch adjustment
- Controls weapon firing logic
- Implements idle scan and recenter behaviors
- Parses turret configuration data

## Key Types
- **TurretStateMachine (Class)**: Manages turret state transitions
- **TurretAIData (Struct)**: Stores turret configuration parameters
- **TurretAI (Class)**: Core turret AI logic
- **TurretAIAimTurretState (Class)**: Handles turret aiming behavior
- **TurretAIIdleState (Class)**: Manages idle turret behavior
- **TurretAIIdleScanState (Class)**: Implements idle scan logic
- **TurretAIHoldTurretState (Class)**: Manages turret hold behavior
- **TurretAIRecenterTurretState (Class)**: Handles turret recenter logic

## Key Functions
### frameToSleepTime
- Purpose: Calculates sleep time based on frame differences
- Calls: TheGameLogic->getFrame()

### parseTWS
- Purpose: Parses weapon slot type configuration
- Calls: INI::scanIndexList()

## Globals
- **WAIT_INDEFINITELY (UnsignedInt)**: Constant for indefinite wait time

## Dependencies
- Common/GameAudio.h
- Common/PerfTimer.h
- Common/RandomValue.h
- Common/ThingTemplate.h
- Common/Xfer.h
- GameLogic/GameLogic.h
- GameLogic/Module/AIUpdate.h
- GameLogic/Object.h
- GameLogic/PartitionManager.h
- GameLogic/TerrainLogic.h
- GameLogic/TurretAI.h
- GameLogic/Weapon.h
- GameLogic/WeaponSet.h
