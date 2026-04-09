# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/SpecialPower/BaikonurLaunchPower.cpp

## Purpose
Implements the Baikonur launch tower special power, triggering the GLA end-game sequence.

## Responsibilities
- Extends `SpecialPowerModule` to handle Baikonur launch mechanics
- Manages detonation object creation at specified location
- Handles model state transitions (door opening)
- Provides INI field parsing for module data

## Key Types
- `BaikonurLaunchPowerModuleData` (Class): Stores detonation object reference
- `BaikonurLaunchPower` (Class): Main power implementation

## Key Functions
### `doSpecialPower`
- Purpose: Initiates launch sequence by opening door model
- Calls: `SpecialPowerModule::doSpecialPower`, `setModelConditionState`

### `doSpecialPowerAtLocation`
- Purpose: Creates detonation object at specified coordinates
- Calls: `SpecialPowerModule::doSpecialPowerAtLocation`, `TheThingFactory` methods

### `buildFieldParse`
- Purpose: Defines INI parsing rules for module data
- Calls: `SpecialPowerModuleData::buildFieldParse`

## Globals
- None

## Dependencies
- `SpecialPowerModule.h` (base class)
- `ThingFactory.h` (object creation)
- `Xfer.h` (serialization)
- `Player.h`, `GameLogic.h`, `Object.h` (game framework)
