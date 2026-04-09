# Generals/Code/GameEngine/Source/GameLogic/Object/Upgrade/StealthUpgrade.cpp

## Purpose
This file implements the `StealthUpgrade` class, which is responsible for applying a stealth upgrade to game objects in Command & Conquer Generals.

## Responsibilities
- Handles the initialization and destruction of stealth upgrades.
- Implements the logic to apply the stealth status to an object.
- Manages serialization (CRC and Xfer) for the stealth upgrade module.

## Key Types
- `StealthUpgrade` (Class): Represents a stealth upgrade that can be applied to game objects, setting their stealth status.

## Key Functions
### StealthUpgrade::upgradeImplementation
- Purpose: Sets the `OBJECT_STATUS_CAN_STEALTH` status on the object.
- Calls:
  - `getObject()`
  - `setStatus(OBJECT_STATUS_CAN_STEALTH)`

### StealthUpgrade::crc
- Purpose: Extends the base class's CRC method for serialization.
- Calls:
  - `UpgradeModule::crc(xfer)`

### StealthUpgrade::xfer
- Purpose: Handles versioned serialization of the stealth upgrade module.
- Calls:
  - `xfer->xferVersion(&version, currentVersion)`
  - `UpgradeModule::xfer(xfer)`

### StealthUpgrade::loadPostProcess
- Purpose: Extends the base class's load post-processing method.
- Calls:
  - `UpgradeModule::loadPostProcess()`

## Globals
None

## Dependencies
- Key includes and external symbols used but not defined here:
  - `PreRTS.h`
  - `Common/Xfer.h`
  - `GameLogic/Module/StealthUpgrade.h`
  - `GameLogic/Object.h`
