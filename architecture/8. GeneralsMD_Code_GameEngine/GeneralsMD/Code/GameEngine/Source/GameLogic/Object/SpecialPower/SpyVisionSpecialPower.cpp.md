# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/SpecialPower/SpyVisionSpecialPower.cpp

## Purpose
Implements the SpyVision special power module, which grants vision of enemy players based on captured units.

## Responsibilities
- Calculates spy vision duration based on captured units
- Activates spy vision updates on the source object
- Handles module data parsing and serialization

## Key Types
- **SpyVisionSpecialPowerModuleData (Class)**: Stores configuration for spy vision duration (base, bonus per captured, max)
- **SpyVisionSpecialPower (Class)**: Manages spy vision special power logic and activation

## Key Functions
### `doSpecialPower`
- Purpose: Activates spy vision based on captured units and module data
- Calls: `SpecialPowerModule::doSpecialPower`, `getContain`, `findUpdateModule`, `activateSpyVision`

### `buildFieldParse`
- Purpose: Defines INI field parsing for module data
- Calls: `SpecialPowerModuleData::buildFieldParse`

### `crc`
- Purpose: Serialization checksum for network sync
- Calls: `SpecialPowerModule::crc`

### `xfer`
- Purpose: Serialization for network sync
- Calls: `SpecialPowerModule::xfer`

### `loadPostProcess`
- Purpose: Post-load initialization
- Calls: `SpecialPowerModule::loadPostProcess`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameLogic/Object.h`, `GameLogic/Module/ContainModule.h`, `GameLogic/Module/SpyVisionSpecialPower.h`, `GameLogic/Module/SpyVisionUpdate.h`
- `SpecialPowerModule`, `SpecialPowerModuleData`, `ContainModuleInterface`, `SpyVisionUpdate`
