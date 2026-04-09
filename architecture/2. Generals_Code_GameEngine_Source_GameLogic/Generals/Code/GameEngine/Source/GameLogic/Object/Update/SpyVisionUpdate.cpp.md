# Generals/Code/GameEngine/Source/GameLogic/Object/Update/SpyVisionUpdate.cpp

## Purpose
This file implements the `SpyVisionUpdate` class, which handles the special power that allows a player to spy on the vision of all enemy players for a specified duration.

## Responsibilities
- Manages the activation and deactivation of the spy vision ability.
- Updates the vision state of enemy players based on the duration of the ability.
- Handles serialization and deserialization of the module's data.

## Key Types
- `SpyVisionUpdateModuleData (struct)`: Stores configuration for the spy vision update module.
- `SpyVisionUpdate (class)`: Manages the logic for activating, updating, and deactivating the spy vision ability.

## Key Functions
### activateSpyVision
- Purpose: Activates the spy vision ability for a specified duration.
- Calls: 
  - `doActivationWork(TRUE)`
  - `setWakeFrame`

### update
- Purpose: Updates the state of the spy vision ability, deactivating it when the duration ends.
- Calls: 
  - `doActivationWork(FALSE)`

### doActivationWork
- Purpose: Toggles the vision spied status for enemy players.
- Calls: None

### onDelete
- Purpose: Ensures the spy vision ability is deactivated if it was still active at the time of deletion.
- Calls: 
  - `doActivationWork(FALSE)`

## Globals
- `None`: No global/static variables are defined in this file.

## Dependencies
- Key includes:
  - `"Common/Player.h"`
  - `"Common/PlayerList.h"`
  - `"GameLogic/GameLogic.h"`
  - `"GameLogic/Module/SpyVisionUpdate.h"`
