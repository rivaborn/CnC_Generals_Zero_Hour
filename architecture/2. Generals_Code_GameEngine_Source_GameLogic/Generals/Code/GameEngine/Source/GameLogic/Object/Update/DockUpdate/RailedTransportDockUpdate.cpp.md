# Generals/Code/GameEngine/Source/GameLogic/Object/Update/DockUpdate/RailedTransportDockUpdate.cpp

## Purpose
This file implements the `RailedTransportDockUpdate` class, which handles the docking and undocking logic for railed transport objects in Command & Conquer Generals. It manages the movement of objects being loaded into and unloaded from a transport.

## Responsibilities
- Manages the docking process for objects entering a railed transport.
- Handles the unloading process for objects exiting a railed transport.
- Ensures proper positioning and orientation of objects during docking and undocking.
- Maintains state information about currently docked or undocked objects.

## Key Types
- `RailedTransportDockUpdateModuleData` (Struct): Stores configuration data for the docking update module, such as durations for pulling inside and pushing outside.
- `UNLOAD_ALL` (Enum): Represents the action to unload all contained objects.

## Key Functions
### RailedTransportDockUpdate::update
- Purpose: Updates the state of the railed transport's docking and undocking processes.
- Calls:
  - `doPullInDocking`
  - `doPushOutDocking`

### RailedTransportDockUpdate::action
- Purpose: Handles the initial action when an object starts docking with the transport.
- Calls:
  - `TheGameLogic->deselectObject`
  - `docker->setStatus`
  - `docker->setDisabled`
  - `docker->setOrientation`

### RailedTransportDockUpdate::unloadAll
- Purpose: Initiates the process of unloading all objects from the transport.
- Calls:
  - `unloadNext`

### RailedTransportDockUpdate::doPullInDocking
- Purpose: Moves an object being docked inside the transport.
- Calls:
  - `TheGameLogic->findObjectByID`
  - `docker->setPosition`
  - `docker->setModelConditionState`
  - `contain->addToContain`

### RailedTransportDockUpdate::doPushOutDocking
- Purpose: Moves an object being undocked outside the transport.
- Calls:
  - `TheGameLogic->findObjectByID`
  - `unloader->setPosition`
  - `unloader->setModelConditionState`
  - `unloaderAI->aiIdle`

### RailedTransportDockUpdate::unloadNext
- Purpose: Starts the process of unloading the next object from the transport.
- Calls:
  - `openContain->iterateContained`
  - `openContain->removeFromContain`
  - `unloader->setPosition`
  - `unloader->setOrientation`
  - `unloader->setDisabled`

## Globals
- None

## Dependencies
- Key includes and external symbols used but not defined here:
  - `PreRTS.h`
  - `ThingTemplate.h`
  - `Xfer.h`
  - `Drawable.h`
  - `InGameUI.h`
  - `GameLogic.h`
  - `Object.h`
  - `PartitionManager.h`
  - `AIUpdate.h`
  - `ContainModule.h`
  - `OpenContain.h`
  - `RailedTransportDockUpdate.h`
