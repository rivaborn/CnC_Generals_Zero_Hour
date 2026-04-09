# Generals/Code/GameEngine/Source/GameLogic/Object/SpecialPower/SpecialAbility.cpp

## Purpose
This file implements the `SpecialAbility` class, which handles special attack processing for units in Command & Conquer Generals.

## Responsibilities
- Manages special power actions at specific locations or objects.
- Extends functionality from the base `SpecialPowerModule`.
- Handles CRC and Xfer operations for data integrity and serialization.

## Key Types
- SpecialAbility (Class): Handles special attack logic for game units.

## Key Functions
### doSpecialPowerAtLocation
- Purpose: Executes a special power at a given location.
- Calls: 
  - `getObject()->isDisabled()`
  - `SpecialPowerModule::doSpecialPowerAtLocation`

### doSpecialPowerAtObject
- Purpose: Executes a special power on a target object.
- Calls:
  - `getObject()->isDisabled()`
  - `SpecialPowerModule::doSpecialPowerAtObject`

### doSpecialPower
- Purpose: Executes a special power with given command options.
- Calls:
  - `getObject()->isDisabled()`
  - `SpecialPowerModule::doSpecialPower`

### crc
- Purpose: Computes the CRC for data integrity.
- Calls:
  - `SpecialPowerModule::crc`

### xfer
- Purpose: Handles serialization and deserialization of the object.
- Calls:
  - `xfer->xferVersion`
  - `SpecialPowerModule::xfer`

### loadPostProcess
- Purpose: Performs post-processing after loading.
- Calls:
  - `SpecialPowerModule::loadPostProcess`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/Player.h"
  - "Common/Xfer.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/SpecialAbility.h"
