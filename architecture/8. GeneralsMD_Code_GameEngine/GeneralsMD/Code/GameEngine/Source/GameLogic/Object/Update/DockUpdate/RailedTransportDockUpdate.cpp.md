# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/DockUpdate/RailedTransportDockUpdate.cpp

## Purpose
Handles docking logic for railed transport vehicles, including pulling objects inside and pushing them out.

## Responsibilities
- Manages docking/unloading of objects via railed transport
- Controls movement of objects during docking process
- Handles containment of objects within transport
- Manages timing and positioning for docking animations

## Key Types
- `RailedTransportDockUpdateModuleData` (Class): Stores configuration data for docking behavior
- `RailedTransportDockUpdate` (Class): Main docking update module implementation
- `UNLOAD_ALL` (Enum): Special value indicating all objects should be unloaded

## Key Functions
### `action`
- Purpose: Handles docking action between transport and object
- Calls: `getPosition`, `setStatus`, `setDisabled`, `setOrientation`, `deselectObject`

### `doPullInDocking`
- Purpose: Pulls docking object into transport
- Calls: `findObjectByID`, `getPosition`, `setPosition`, `setModelConditionState`, `clearModelConditionState`, `cancelDock`, `aiIdle`, `addToContain`

### `doPushOutDocking`
- Purpose: Pushes unloading object out of transport
- Calls: `findObjectByID`, `getPosition`, `setPosition`, `clearModelConditionState`, `aiIdle`, `clearDisabled`, `clearStatus`, `aiMoveToPosition`

### `unloadNext`
- Purpose: Initiates unloading of next contained object
- Calls: `getContain`, `asOpenContain`, `iterateContained`, `removeFromContain`, `setPosition`, `setOrientation`, `setDisabled`, `getExitPosition`

## Globals
- None

## Dependencies
- `PreRTS.h`, `ThingTemplate.h`, `Xfer.h`, `Drawable.h`, `InGameUI.h`, `GameLogic.h`, `Object.h`, `PartitionManager.h`, `AIUpdate.h`, `ContainModule.h`, `OpenContain.h`, `RailedTransportDockUpdate.h`
