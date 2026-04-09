# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Create/VeterancyGainCreate.cpp

## Purpose
Handles setting an object's veterancy level during creation if the required science is known.

## Responsibilities
- Parses veterancy configuration from INI files
- Checks player's science knowledge
- Sets minimum veterancy level for trainable objects
- Implements serialization (CRC, Xfer, loadPostProcess)

## Key Types
- `VeterancyGainCreateModuleData` (Class): Stores veterancy configuration (starting level, required science)
- `VeterancyGainCreate` (Class): Module that applies veterancy on object creation

## Key Functions
### `VeterancyGainCreateModuleData::buildFieldParse`
- Purpose: Registers INI field parsers for veterancy data
- Calls: `CreateModuleData::buildFieldParse`

### `VeterancyGainCreate::onCreate`
- Purpose: Applies veterancy level if science requirements are met
- Calls: `getVeterancyGainCreateModuleData`, `getObject`, `getControllingPlayer`, `hasScience`, `getExperienceTracker`, `isTrainable`, `setMinVeterancyLevel`

### `VeterancyGainCreate::crc`
- Purpose: Serialization checksum for network sync
- Calls: `CreateModule::crc`

### `VeterancyGainCreate::xfer`
- Purpose: Serialization for save/load
- Calls: `CreateModule::xfer`

### `VeterancyGainCreate::loadPostProcess`
- Purpose: Post-processing after loading
- Calls: `CreateModule::loadPostProcess`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/Player.h`, `Common/Xfer.h`, `GameLogic/ExperienceTracker.h`, `GameLogic/Object.h`, `GameLogic/
