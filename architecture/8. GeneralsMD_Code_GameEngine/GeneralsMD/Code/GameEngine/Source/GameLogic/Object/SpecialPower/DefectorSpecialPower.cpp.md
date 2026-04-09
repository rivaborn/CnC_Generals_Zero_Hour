# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/SpecialPower/DefectorSpecialPower.cpp

## Purpose
Implements the "Defector" special power, allowing a general to convert enemy units to their side.

## Responsibilities
- Handles defection logic for enemy units
- Manages special power activation at objects
- Extends base SpecialPowerModule functionality
- Serialization (CRC, Xfer) for save/load

## Key Types
- **DefectorSpecialPowerModuleData (Class)**: Holds module-specific data (e.g., cursor radius)
- **DefectorSpecialPower (Class)**: Implements the defector special power behavior

## Key Functions
### `doSpecialPowerAtObject`
- Purpose: Converts the target object to the player's team
- Calls: `SpecialPowerModule::doSpecialPowerAtObject`, `objectToMakeDefector->defect`

### `crc`
- Purpose: Serialization checksum for save/load
- Calls: `SpecialPowerModule::crc`

### `xfer`
- Purpose: Serialization for save/load
- Calls: `SpecialPowerModule::xfer`

### `loadPostProcess`
- Purpose: Post-load initialization
- Calls: `SpecialPowerModule::loadPostProcess`

## Globals
- **None**

## Dependencies
- `SpecialPowerModule`, `Object`, `Player`, `Team`, `Xfer`, `MultiIniFieldParse`
- `DefectorSpecialPowerModuleData`, `SpecialPowerTemplate`
