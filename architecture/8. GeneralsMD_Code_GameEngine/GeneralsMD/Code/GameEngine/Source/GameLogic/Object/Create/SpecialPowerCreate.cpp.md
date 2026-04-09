# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Create/SpecialPowerCreate.cpp

## Purpose
Handles creation and initialization of special power modules when a building is created.

## Responsibilities
- Initializes special power modules on building creation
- Triggers special power countdowns when buildings complete construction
- Manages serialization (Xfer) and CRC for special power creation data
- Extends base `CreateModule` functionality

## Key Types
- **SpecialPowerCreate (Class)**: Manages special power creation logic for buildings
- **SpecialPowerModuleInterface (Type)**: Interface for special power modules

## Key Functions
### `onBuildComplete`
- Purpose: Activates special power modules when a building finishes construction
- Calls: `shouldDoOnBuildComplete`, `CreateModule::onBuildComplete`, `getObject`, `getBehaviorModules`, `getSpecialPower`, `onSpecialPowerCreation`

### `crc`
- Purpose: Serializes CRC data for special power creation
- Calls: `CreateModule::crc`

### `xfer`
- Purpose: Handles serialization/deserialization of special power creation data
- Calls: `CreateModule::xfer`

### `loadPostProcess`
- Purpose: Post-processing after loading special power creation data
- Calls: `CreateModule::loadPostProcess`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameLogic/Object.h`, `GameLogic/Module/SpecialPowerCreate.h`, `GameLogic/Module/SpecialPowerModule.h`
- `Thing`, `ModuleData`, `BehaviorModule`, `Xfer`, `XferVersion`
