# Generals/Code/GameEngine/Source/GameLogic/Object/SpecialPower/CleanupAreaPower.cpp

## Purpose
This file implements the `CleanupAreaPower` class, which manages a special power that cleans up an area by expanding its range until nothing is left to clean.

## Responsibilities
- Manages the cleanup area power for game objects.
- Sets parameters for the cleanup hazard update module.
- Handles serialization and deserialization of the module data.

## Key Types
- `CleanupAreaPowerModuleData (struct)`: Stores configuration data for the cleanup area power, such as move range.
- `CleanupAreaPower (class)`: Implements the logic for the cleanup area power special ability.

## Key Functions
### CleanupAreaPower::doSpecialPowerAtLocation
- Purpose: Activates the cleanup power at a specified location.
- Calls:
  - `getObject()->isDisabled()`
  - `findUpdateModule`
  - `setCleanupAreaParameters`

### CleanupAreaPower::crc
- Purpose: Computes the CRC for the module data.
- Calls:
  - `SpecialPowerModule::crc`

### CleanupAreaPower::xfer
- Purpose: Handles serialization and deserialization of the module data.
- Calls:
  - `xferVersion`
  - `SpecialPowerModule::xfer`

### CleanupAreaPower::loadPostProcess
- Purpose: Performs post-processing after loading the module data.
- Calls:
  - `SpecialPowerModule::loadPostProcess`

## Globals
- None

## Dependencies
- Includes:
  - "Common/Player.h"
  - "Common/ThingTemplate.h"
  - "Common/Xfer.h"
  - "GameLogic/Module/CleanupAreaPower.h"
  - "GameLogic/Module/CleanupHazardUpdate.h"
  - "GameLogic/Object.h"
