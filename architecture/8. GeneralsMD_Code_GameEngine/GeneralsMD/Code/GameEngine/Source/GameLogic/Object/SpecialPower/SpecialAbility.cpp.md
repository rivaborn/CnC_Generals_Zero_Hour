# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/SpecialPower/SpecialAbility.cpp

## Purpose
Handles processing of special attacks from units, extending base special power functionality.

## Responsibilities
- Extends `SpecialPowerModule` with additional special attack logic
- Manages special power execution at locations, objects, or generally
- Handles serialization (Xfer) and CRC for network sync
- Performs post-load initialization

## Key Types
- `SpecialAbility` (Class): Extends special power functionality for unit attacks

## Key Functions
### `doSpecialPowerAtLocation`
- Purpose: Executes special power at a specific location
- Calls: `SpecialPowerModule::doSpecialPowerAtLocation`

### `doSpecialPowerAtObject`
- Purpose: Executes special power targeting an object
- Calls: `SpecialPowerModule::doSpecialPowerAtObject`

### `doSpecialPower`
- Purpose: Executes general special power action
- Calls: `SpecialPowerModule::doSpecialPower`

### `crc`
- Purpose: Serializes class data for CRC calculation
- Calls: `SpecialPowerModule::crc`

### `xfer`
- Purpose: Handles network serialization
- Calls: `SpecialPowerModule::xfer`

### `loadPostProcess`
- Purpose: Performs post-load initialization
- Calls: `SpecialPowerModule::loadPostProcess`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/Player.h`, `Common/Xfer.h`, `GameLogic/Object.h`, `GameLogic/Module/SpecialAbility.h`
- `Thing`, `ModuleData`, `Coord3D`, `Real`, `UnsignedInt`, `Xfer`, `XferVersion`, `Object`, `SpecialPowerModule`
