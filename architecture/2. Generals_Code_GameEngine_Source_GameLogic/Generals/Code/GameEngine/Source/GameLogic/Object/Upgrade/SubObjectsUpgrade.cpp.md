# Generals/Code/GameEngine/Source/GameLogic/Object/Upgrade/SubObjectsUpgrade.cpp

## Purpose
This file implements the logic for showing or hiding subobjects of game objects based on upgrade status, overriding any animation states.

## Responsibilities
- Parses configuration data for subobject visibility.
- Manages the upgrade process to show or hide specified subobjects.
- Handles CRC and Xfer operations for serialization.

## Key Types
- `SubObjectsUpgradeModuleData (struct)`: Stores configuration for showing and hiding subobjects.
- `SubObjectsUpgrade (class)`: Inherits from `UpgradeModule` and implements the logic for subobject visibility based on upgrades.

## Key Functions
### buildFieldParse
- Purpose: Sets up field parsing for subobject upgrade data.
- Calls: `UpgradeModuleData::buildFieldParse`

### SubObjectsUpgrade
- Purpose: Constructor for the `SubObjectsUpgrade` class.
- Calls: None

### ~SubObjectsUpgrade
- Purpose: Destructor for the `SubObjectsUpgrade` class.
- Calls: None

### upgradeImplementation
- Purpose: Implements the logic to show or hide subobjects based on upgrade status.
- Calls: `getSubObjectsUpgradeModuleData`, `getObject()->getObjectCompletedUpgradeMask()`, `getObject()->getControllingPlayer()->getCompletedUpgradeMask()`, `getDrawable()->showSubObject`, `getDrawable()->updateSubObjects`

### crc
- Purpose: Handles CRC operations for the module.
- Calls: `UpgradeModule::crc`

### xfer
- Purpose: Handles Xfer (serialization) operations for the module.
- Calls: `xfer->xferVersion`, `UpgradeModule::xfer`

### loadPostProcess
- Purpose: Post-processing after loading the module.
- Calls: `UpgradeModule::loadPostProcess`

## Globals
- None

## Dependencies
- Key includes:
  - `"PreRTS.h"`
  - `"Common/Player.h"`
  - `"Common
