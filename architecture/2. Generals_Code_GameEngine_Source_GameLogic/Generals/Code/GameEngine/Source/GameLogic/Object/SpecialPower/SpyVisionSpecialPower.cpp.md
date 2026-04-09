# Generals/Code/GameEngine/Source/GameLogic/Object/SpecialPower/SpyVisionSpecialPower.cpp

## Purpose
This file implements the `SpyVisionSpecialPower` class, which handles the special power allowing a player to spy on enemy vision.

## Responsibilities
- Manages the activation and duration of the spy vision special power.
- Extends functionality from the base `SpecialPowerModule`.
- Parses configuration data for the special power's duration settings.

## Key Types
- **SpyVisionSpecialPowerModuleData (struct)**: Stores configuration data for the spy vision special power, including base duration, bonus duration per captured unit, and maximum duration.
- **SpyVisionSpecialPower (class)**: Handles the logic for activating and managing the spy vision special power.

## Key Functions
### doSpecialPower
- Purpose: Activates the spy vision special power.
- Calls:
  - `getObject()->isDisabled()`
  - `SpecialPowerModule::doSpecialPower(commandOptions)`
  - `getContainCount()`
  - `activateSpyVision(duration)`

### crc
- Purpose: Computes the CRC for the module data.
- Calls:
  - `SpecialPowerModule::crc(xfer)`

### xfer
- Purpose: Handles serialization and deserialization of the module data.
- Calls:
  - `xfer->xferVersion(&version, currentVersion)`
  - `SpecialPowerModule::xfer(xfer)`

### loadPostProcess
- Purpose: Performs post-load processing for the module.
- Calls:
  - `SpecialPowerModule::loadPostProcess()`

## Globals
- None

## Dependencies
- Key includes:
  - "Common/Xfer.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/ContainModule.h"
  - "GameLogic/Module/SpyVisionSpecialPower.h"
  - "GameLogic/Module/SpyVisionUpdate.h"
