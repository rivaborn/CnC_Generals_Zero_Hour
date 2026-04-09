# Generals/Code/GameEngine/Source/GameLogic/Object/SpecialPower/DefectorSpecialPower.cpp

## Purpose
This file implements the logic for the "Defector" special power, allowing a general to capture enemy units and make them part of their team.

## Responsibilities
- Handles the initialization and configuration of the Defector special power.
- Manages the execution of the special power when applied to an object.
- Implements CRC and Xfer methods for data serialization.

## Key Types
- **DefectorSpecialPowerModuleData (struct)**: Stores configuration data for the Defector special power, such as cursor radius.
- **DefectorSpecialPower (class)**: Manages the behavior of the Defector special power when activated.

## Key Functions
### DefectorSpecialPower::doSpecialPowerAtObject
- Purpose: Executes the Defector special power on a target object.
- Calls:
  - `getObject()->isDisabled()`
  - `SpecialPowerModule::doSpecialPowerAtObject`
  - `getSpecialPowerTemplate()->getDetectionTime()`
  - `objectToMakeDefector->defect`

### DefectorSpecialPower::crc
- Purpose: Implements CRC for the Defector special power.
- Calls:
  - `SpecialPowerModule::crc`

### DefectorSpecialPower::xfer
- Purpose: Implements Xfer method for data serialization of the Defector special power.
- Calls:
  - `xfer->xferVersion`
  - `SpecialPowerModule::xfer`

## Globals
- None

## Dependencies
- Includes:
  - "PreRTS.h"
  - "Common/Player.h"
  - "Common/SpecialPower.h"
  - "Common/Team.h"
  - "Common/Xfer.h"
  - "GameLogic/Module/DefectorSpecialPower.h"
  - "GameLogic/Object.h"
