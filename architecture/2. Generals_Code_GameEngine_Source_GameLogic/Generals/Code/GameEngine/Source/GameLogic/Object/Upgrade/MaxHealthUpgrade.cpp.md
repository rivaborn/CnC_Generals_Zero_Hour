# Generals/Code/GameEngine/Source/GameLogic/Object/Upgrade/MaxHealthUpgrade.cpp

## Purpose
This file implements the `MaxHealthUpgrade` class, which is an upgrade module that modifies an object's maximum health.

## Responsibilities
- Handles the initialization and destruction of the `MaxHealthUpgrade` module.
- Implements the logic to increase an object's maximum health based on specified parameters.
- Manages serialization (CRC and Xfer) for the module data.

## Key Types
- **MaxHealthUpgradeModuleData (struct)**: Stores configuration data for the max health upgrade, including the amount of health to add and the type of change.
- **MaxHealthUpgrade (class)**: Inherits from `UpgradeModule` and implements the specific logic for modifying an object's maximum health.

## Key Functions
### MaxHealthUpgrade::upgradeImplementation
- Purpose: Increases the object's maximum health by a specified scalar value.
- Calls:
  - getMaxHealthUpgradeModuleData()
  - getObject()
  - getBodyModule()
  - setMaxHealth()

### MaxHealthUpgrade::crc
- Purpose: Extends the base class CRC method to include module-specific data.
- Calls:
  - UpgradeModule::crc()

### MaxHealthUpgrade::xfer
- Purpose: Handles serialization of the `MaxHealthUpgrade` module data.
- Calls:
  - xferVersion()
  - UpgradeModule::xfer()

### MaxHealthUpgrade::loadPostProcess
- Purpose: Extends the base class post-load processing.
- Calls:
  - UpgradeModule::loadPostProcess()

## Globals
- None

## Dependencies
- **Includes**:
  - "PreRTS.h"
  - "Common/Xfer.h"
  - "GameLogic/Object.h"
  - "GameLogic/ExperienceTracker.h"
  - "GameLogic/Module/MaxHealthUpgrade.h"
  - "GameLogic/Module/BodyModule.h"

- **External Symbols**:
