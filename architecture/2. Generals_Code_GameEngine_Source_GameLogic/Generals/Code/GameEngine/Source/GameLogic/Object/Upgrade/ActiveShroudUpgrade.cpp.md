# Generals/Code/GameEngine/Source/GameLogic/Object/Upgrade/ActiveShroudUpgrade.cpp

## Purpose
This file implements the `ActiveShroudUpgrade` class, which modifies an object's shroud range through an upgrade.

## Responsibilities
- Handles the initialization and destruction of the active shroud upgrade.
- Implements the upgrade logic to change the object's shroud range.
- Manages CRC and Xfer operations for data persistence.

## Key Types
- `ActiveShroudUpgradeModuleData (struct)`: Stores new shroud range data.
- `ActiveShroudUpgrade (class)`: Represents the active shroud upgrade module.

## Key Functions
### ActiveShroudUpgrade::upgradeImplementation
- Purpose: Sets the object's shroud range to the new value specified by the upgrade.
- Calls:
  - `getObject()->setShroudRange`
  - `getObject()->handlePartitionCellMaintenance`

### ActiveShroudUpgrade::crc
- Purpose: Extends base class CRC functionality.
- Calls: `UpgradeModule::crc`

### ActiveShroudUpgrade::xfer
- Purpose: Handles data transfer for persistence, including versioning.
- Calls: `UpgradeModule::xfer`

### ActiveShroudUpgrade::loadPostProcess
- Purpose: Extends base class post-load processing.
- Calls: `UpgradeModule::loadPostProcess`

## Globals
None

## Dependencies
- Includes:
  - "PreRTS.h"
  - "Common/Xfer.h"
  - "GameLogic/Module/ActiveShroudUpgrade.h"
  - "GameLogic/Object.h"
