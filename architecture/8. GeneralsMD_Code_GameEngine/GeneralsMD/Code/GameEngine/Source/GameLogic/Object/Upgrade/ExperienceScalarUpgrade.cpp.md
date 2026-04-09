# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/ExperienceScalarUpgrade.cpp

## Purpose
Implements an upgrade module that modifies an object's experience gain by applying a scalar multiplier.

## Responsibilities
- Defines `ExperienceScalarUpgradeModuleData` to store the XP scalar value.
- Implements `ExperienceScalarUpgrade` class to apply the scalar to the object's `ExperienceTracker`.
- Handles serialization (Xfer) and CRC for network sync.
- Parses INI configuration for the scalar value.

## Key Types
- `ExperienceScalarUpgradeModuleData` (struct): Stores the XP scalar value (`m_addXPScalar`).
- `ExperienceScalarUpgrade` (class): Upgrade module that applies the scalar to the object's XP tracker.

## Key Functions
### `ExperienceScalarUpgradeModuleData::buildFieldParse`
- Purpose: Registers INI field parsing for `m_addXPScalar`.
- Calls: `UpgradeModuleData::buildFieldParse`.

### `ExperienceScalarUpgrade::upgradeImplementation`
- Purpose: Applies the XP scalar to the object's `ExperienceTracker`.
- Calls: `getExperienceScalarUpgradeModuleData`, `getObject`, `getExperienceTracker`, `setExperienceScalar`.

### `ExperienceScalarUpgrade::crc`
- Purpose: Serializes CRC data for network sync.
- Calls: `UpgradeModule::crc`.

### `ExperienceScalarUpgrade::xfer`
- Purpose: Handles Xfer serialization (version 1).
- Calls: `UpgradeModule::xfer`.

## Globals
- None.

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameLogic/Object.h`, `GameLogic/ExperienceTracker.h`, `GameLogic/Module/ExperienceScalarUpgrade.h`.
- Uses `MultiIniFieldParse`, `INI::parseReal`, `Xfer`, `Thing`, `Object`, `ExperienceTracker`.
