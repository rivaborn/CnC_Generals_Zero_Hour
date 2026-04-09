# Generals/Code/GameEngine/Source/GameLogic/Object/Upgrade/StatusBitsUpgrade.cpp

## Purpose
This file implements the `StatusBitsUpgrade` class, which handles upgrading objects by setting or clearing specific status bits.

## Responsibilities
- Parses configuration data for status bits to set and clear.
- Manages the upgrade process by modifying object status bits.
- Implements CRC and Xfer methods for serialization.

## Key Types
- **StatusBitsUpgradeModuleData (struct)**: Stores configuration data for status bits to set and clear.
- **StatusBitsUpgrade (class)**: Inherits from `UpgradeModule` and manages the actual upgrade logic.

## Key Functions
### buildFieldParse
- Purpose: Parses INI fields for status bits to set and clear.
- Calls: `UpgradeModuleData::buildFieldParse`, `INI::parseBitString32`

### StatusBitsUpgrade (constructor)
- Purpose: Initializes the `StatusBitsUpgrade` module.
- Calls: None

### ~StatusBitsUpgrade (destructor)
- Purpose: Cleans up the `StatusBitsUpgrade` module.
- Calls: None

### upgradeImplementation
- Purpose: Sets and clears object status bits based on configuration.
- Calls: `Object::setStatus`, `Object::clearStatus`

### crc
- Purpose: Implements CRC method for serialization.
- Calls: `UpgradeModule::crc`

### xfer
- Purpose: Implements Xfer method for serialization, including version handling.
- Calls: `xfer->xferVersion`, `UpgradeModule::xfer`

### loadPostProcess
- Purpose: Handles post-processing after loading.
- Calls: `UpgradeModule::loadPostProcess`

## Globals
- None

## Dependencies
- **Includes**:
  - "PreRTS.h"
  - "Common/Xfer.h"
  - "GameClient/Drawable.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/StatusBitsUpgrade.h"
