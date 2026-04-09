# Generals/Code/GameEngine/Source/GameLogic/Object/Update/DynamicGeometryInfoUpdate.cpp

## Purpose
This file contains the implementation of a module that updates an object's geometry information dynamically over time, including height and radius changes.

## Responsibilities
- Handles dynamic updates to an object's geometry.
- Manages transitions between initial and final geometry states.
- Supports optional reversal of the transition at the midpoint.

## Key Types
- **DynamicGeometryInfoUpdateModuleData (struct):** Stores configuration data for the geometry update, including initial and final dimensions, delay, and transition time.
- **DynamicGeometryInfoUpdate (class):** Implements the dynamic geometry update logic, inheriting from `UpdateModule`.

## Key Functions
### DynamicGeometryInfoUpdate::update
- Purpose: Updates the object's geometry over time according to specified parameters.
- Calls:
  - `getObject()`
  - `getGeometryInfo()`
  - `setGeometryInfo()`

### DynamicGeometryInfoUpdate::crc
- Purpose: Computes a CRC for the module data.
- Calls:
  - `UpdateModule::crc()`

### DynamicGeometryInfoUpdate::xfer
- Purpose: Handles serialization and deserialization of the module's state.
- Calls:
  - `UpdateModule::xfer()`
  - Various `xfer->xfer*` methods

## Globals
- None

## Dependencies
- **Includes:**
  - "PreRTS.h"
  - "Common/Xfer.h"
  - "GameLogic/Module/DynamicGeometryInfoUpdate.h"
  - "GameLogic/Object.h"

- **External Symbols Used:**
  - `Thing`
  - `ModuleData`
  - `MultiIniFieldParse`
  - `INI::parseDurationUnsignedInt`
  - `INI::parseReal`
  - `INI::parseBool`
  - `UpdateModule`
  - `UPDATE_SLEEP_NONE`
  - `XferVersion`
  - `GeometryInfo`
