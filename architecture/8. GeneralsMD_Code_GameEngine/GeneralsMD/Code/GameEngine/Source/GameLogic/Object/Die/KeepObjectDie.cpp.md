# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Die/KeepObjectDie.cpp

## Purpose
Handles destruction logic for objects that should leave rubble without using other die modules, specifically for civilian buildings lacking garrison functionality.

## Responsibilities
- Manages object destruction while preserving rubble
- Implements die callback with damage applicability check
- Provides serialization (Xfer) and CRC support
- Handles post-load processing

## Key Types
- `KeepObjectDie` (Class): Die module for rubble-preserving destruction

## Key Functions
### `KeepObjectDie::onDie`
- Purpose: Handles object destruction while checking damage applicability
- Calls: `isDieApplicable`

### `KeepObjectDie::crc`
- Purpose: Serializes class data for CRC calculation
- Calls: `DieModule::crc`

### `KeepObjectDie::xfer`
- Purpose: Serializes class data for network transfer
- Calls: `DieModule::xfer`

### `KeepObjectDie::loadPostProcess`
- Purpose: Handles post-load initialization
- Calls: `DieModule::loadPostProcess`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameClient/Drawable.h`, `GameLogic/GameLogic.h`, `GameLogic/Module/KeepObjectDie.h`
- `DieModule`, `Thing`, `ModuleData`, `DamageInfo`, `Xfer`, `XferVersion`
