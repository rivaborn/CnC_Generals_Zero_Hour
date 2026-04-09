# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/ModelConditionUpgrade.cpp

## Purpose
Implements an upgrade module that sets a model condition flag on an object.

## Responsibilities
- Defines `ModelConditionUpgradeModuleData` to store condition flag
- Implements `ModelConditionUpgrade` class to apply the condition
- Handles INI field parsing for the condition flag
- Provides serialization (Xfer) and CRC support

## Key Types
- `ModelConditionUpgradeModuleData` (struct): Stores the model condition flag
- `ModelConditionUpgrade` (class): Upgrade module that sets model conditions

## Key Functions
### `ModelConditionUpgradeModuleData::buildFieldParse`
- Purpose: Registers INI field parsing for the condition flag
- Calls: `UpgradeModuleData::buildFieldParse`

### `ModelConditionUpgrade::upgradeImplementation`
- Purpose: Applies the model condition flag to the object
- Calls: `getModelConditionUpgradeModuleData`, `getObject`, `setModelConditionState`

### `ModelConditionUpgrade::crc`
- Purpose: Serializes/deserializes CRC data
- Calls: `UpgradeModule::crc`

### `ModelConditionUpgrade::xfer`
- Purpose: Handles object serialization
- Calls: `UpgradeModule::xfer`

## Globals
- None

## Dependencies
- `PreRTS.h`, `ModelConditionUpgrade.h`, `ModelState.h`, `Object.h`
- `MultiIniFieldParse`, `ModelConditionFlags`, `UpgradeModuleData`, `UpgradeModule`, `Thing`, `Object`, `Xfer`, `XferVersion`
