# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/StealthUpdate.cpp

## Purpose
Handles stealth and disguise mechanics for game objects, including visibility, detection, and transitions.

## Responsibilities
- Manages stealth state and visibility based on game rules
- Handles disguise mechanics (visual and functional)
- Processes detection and reveal logic
- Synchronizes stealth state across networked games

## Key Types
- **StealthUpdateModuleData (struct)**: Configuration for stealth behavior
- **StealthUpdate (class)**: Core stealth/disguise update module
- **StealthLookType (enum)**: Visual stealth states

## Key Functions
### `isBlackMarket`
- Purpose: Checks if an object is an active Black Market
- Calls: None

### `setWakeupIfInRange`
- Purpose: Wakes up AI units that can detect the stealthed object
- Calls: `ai->wakeUpAndAttemptToTarget()`

### `receiveGrant`
- Purpose: Activates/deactivates stealth via special powers
- Calls: `obj->setStatus()`, `setWakeFrame()`, `riderStealth->receiveGrant()`

### `markAsDetected`
- Purpose: Handles detection logic and reveal effects
- Calls: `disguiseAsObject()`, `player->iterateObjects()`

### `disguiseAsObject`
- Purpose: Initiates/removes visual disguise
- Calls: `changeVisualDisguise()`, `TheControlBar->markUIDirty()`

## Globals
- None

## Dependencies
- Game state: `GameState.h`, `Player.h`, `Radar.h`
- Rendering: `Drawable.h`, `FXList.h`
- Game logic: `Object.h`, `Weapon.h`, `PartitionManager.h`
- Modules: `AIUpdate.h`, `PhysicsUpdate.h`, `ContainModule.h`
- Networking: `Xfer.h`
