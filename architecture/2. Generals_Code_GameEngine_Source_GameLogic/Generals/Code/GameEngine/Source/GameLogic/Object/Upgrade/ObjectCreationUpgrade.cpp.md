# Generals/Code/GameEngine/Source/GameLogic/Object/Upgrade/ObjectCreationUpgrade.cpp

## Purpose
This file implements the logic for upgrades that spawn Object Creation Lists (OCLs), allowing game objects to create other objects upon upgrade.

## Responsibilities
- Manages object creation upgrades.
- Parses configuration data for OCLs.
- Handles the spawning of objects defined in OCLs during an upgrade.

## Key Types
- `ObjectCreationUpgradeModuleData`: Stores data related to object creation upgrades, including the OCL.
- `ObjectCreationUpgrade`: Represents the upgrade module that handles the actual creation of objects from an OCL.

## Key Functions
### ObjectCreationUpgrade::upgradeImplementation
- Purpose: Spawns objects defined in the associated OCL during an upgrade.
- Calls:
  - `getObjectCreationUpgradeModuleData()`
  - `ObjectCreationList::create`

### ObjectCreationUpgrade::crc
- Purpose: Handles CRC (Cyclic Redundancy Check) operations for the module.
- Calls:
  - `UpgradeModule::crc`

### ObjectCreationUpgrade::xfer
- Purpose: Manages data transfer (serialization/deserialization) for the module.
- Calls:
  - `xfer->xferVersion`
  - `UpgradeModule::xfer`

## Globals
None

## Dependencies
- Includes:
  - "PreRTS.h"
  - "Common/ModelState.h"
  - "Common/Player.h"
  - "Common/Xfer.h"
  - "GameClient/Drawable.h"
  - "GameLogic/Module/ObjectCreationUpgrade.h"
  - "GameLogic/Object.h"
  - "GameLogic/ObjectCreationList.h"
