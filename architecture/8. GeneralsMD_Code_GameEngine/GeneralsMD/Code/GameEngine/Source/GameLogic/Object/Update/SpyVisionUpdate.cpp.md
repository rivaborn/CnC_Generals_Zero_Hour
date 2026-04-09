# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/SpyVisionUpdate.cpp

## Purpose
Handles the spy vision special power that allows a player to see enemy units.

## Responsibilities
- Activates/deactivates spy vision for a player
- Manages timing for spy vision duration and intervals
- Handles player capture and object deletion events
- Serializes/deserializes spy vision state

## Key Types
- `SpyVisionUpdate` (Class): Manages spy vision functionality for a game object
- `SpyVisionUpdateModuleData` (Struct): Configuration data for spy vision behavior

## Key Functions
### `activateSpyVision`
- Purpose: Activates spy vision for a duration
- Calls: `doActivationWork`, `setWakeFrame`

### `update`
- Purpose: Updates spy vision state each frame
- Calls: `doActivationWork`, `getSpyVisionUpdateModuleData`

### `doActivationWork`
- Purpose: Applies or removes spy vision for enemy players
- Calls: `Player::setUnitsVisionSpied`

### `onCapture`
- Purpose: Handles spy vision transfer when object is captured
- Calls: `doActivationWork`

### `xfer`
- Purpose: Serializes spy vision state
- Calls: `UpdateModule::xfer`

## Globals
- `TheGameLogic` (GameLogic*): Access to game state
- `ThePlayerList` (PlayerList*): List of all players

## Dependencies
- `UpdateModule` (base class)
- `Player`, `PlayerList`, `Xfer`, `GameLogic`
- `SpyVisionUpdateModuleData` (module data struct)
