# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/FlammableUpdate.cpp

## Purpose
Manages the aflame and burned statuses of objects and their associated effects in the game.

## Responsibilities
- Handles ignition, burning, and damage from flames
- Manages flame-related audio events
- Tracks flame damage thresholds and timers
- Updates object status and model conditions
- Interfaces with fire spread mechanics

## Key Types
- **FlammableUpdateModuleData (struct)**: Contains configuration data for flame behavior (durations, damage, sounds)
- **FlammabilityStatusType (enum)**: Tracks object's flame state (normal, aflame, burned)
- **FlammableUpdate (class)**: Main update module handling flame logic

## Key Functions
### `tryToIgnite()`
- Purpose: Initiates burning state for the object
- Calls: `getObject()`, `setStatus()`, `getBodyModule()`, `setAflame()`, `setModelConditionState()`, `startBurningSound()`, `findUpdateModule()`, `startFireSpreading()`, `setWakeFrame()`

### `update()`
- Purpose: Updates flame state and applies damage over time
- Calls: `getObject()`, `getStatusBits()`, `test()`, `setStatus()`, `setModelConditionState()`, `clearStatus()`, `getBodyModule()`, `setAflame()`, `clearModelConditionState()`, `doAflameDamage()`, `calcSleepTime()`

### `onDamage()`
- Purpose: Handles damage events to determine if object should ignite
- Calls: `TheGameLogic->getFrame()`, `getFlammableUpdateModuleData()`, `getObject()`, `getStatusBits()`, `test()`, `tryToIgnite()`

## Globals
- **TheGameLogic (GameLogic**)**: Global game logic instance
- **TheAudio (GameAudio**)**: Global audio system instance

## Dependencies
- `PreRTS.h`, `Common/AudioEventRTS.h`, `Common/GameAudio.h`, `Common/Xfer.h`
- `GameLogic/GameLogic.h`, `GameLogic/Object.h`
- `GameLogic/Module/BodyModule.h`, `GameLogic/Module/FlammableUpdate.h`, `GameLogic/Module/FireSpreadUpdate.h`
