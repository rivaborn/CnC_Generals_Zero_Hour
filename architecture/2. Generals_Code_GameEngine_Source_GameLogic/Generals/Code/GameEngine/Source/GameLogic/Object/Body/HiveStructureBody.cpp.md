# Generals/Code/GameEngine/Source/GameLogic/Object/Body/HiveStructureBody.cpp

## Purpose
This file implements the logic for `HiveStructureBody`, a module that allows structures to propagate specified damage types to their slaves or absorb them if no slaves are available.

## Responsibilities
- Handle damage propagation to slave objects.
- Absorb certain damage types if no slaves are present.
- Manage CRC and Xfer operations for data persistence.

## Key Types
- `HiveStructureBodyModuleData (struct)`: Stores configuration for damage propagation and absorption.
- `HiveStructureBody (class)`: Implements the logic for hive structure bodies.

## Key Functions
### HiveStructureBody::attemptDamage
- Purpose: Determines whether to propagate or absorb incoming damage based on configuration and availability of slaves.
- Calls:
  - `getHiveStructureBodyModuleData()`
  - `getObject()`
  - `getDamageTypeFlag()`
  - `findObjectByID()`
  - `getClosestSlave()`
  - `attemptDamage()` (on slave object)
  - `DEBUG_CRASH()`

### HiveStructureBody::crc
- Purpose: Extends the CRC calculation to include hive-specific data.
- Calls:
  - `StructureBody::crc()`

### HiveStructureBody::xfer
- Purpose: Handles versioned data transfer for persistence.
- Calls:
  - `xferVersion()`
  - `StructureBody::xfer()`

### HiveStructureBody::loadPostProcess
- Purpose: Extends post-load processing to handle hive-specific logic.
- Calls:
  - `StructureBody::loadPostProcess()`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/Xfer.h"
  - "Common/ThingTemplate.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic
