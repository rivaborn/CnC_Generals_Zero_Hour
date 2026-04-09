# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Die/DamDie.cpp

## Purpose
Handles the destruction logic for the water dam object in the game.

## Responsibilities
- Implements dam destruction behavior
- Enables water wave objects when dam is destroyed
- Manages module data for dam destruction
- Provides serialization support (CRC, Xfer)

## Key Types
- **DamDieModuleData (Class)**: Holds data for dam destruction module
- **DamDie (Class)**: Implements dam destruction behavior

## Key Functions
### DamDie::onDie
- Purpose: Activates water wave objects when dam is destroyed
- Calls: `isDieApplicable`, `TheGameLogic->getFirstObject`, `obj->isKindOf`, `obj->clearDisabled`

### DamDieModuleData::buildFieldParse
- Purpose: Sets up field parsing for module data
- Calls: `DieModuleData::buildFieldParse`

### DamDie::crc
- Purpose: Serialization CRC calculation
- Calls: `DieModule::crc`

### DamDie::xfer
- Purpose: Serialization support
- Calls: `DieModule::xfer`

### DamDie::loadPostProcess
- Purpose: Post-load initialization
- Calls: `DieModule::loadPostProcess`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/RandomValue.h`, `Common/Xfer.h`, `GameClient/ParticleSys.h`, `GameClient/TerrainVisual.h`, `GameLogic/GameLogic.h`, `GameLogic/Object.h`, `GameLogic/Module/AIUpdate.h`, `GameLogic/Module/DamDie.h`
- `MultiIniFieldParse`, `DieModuleData`, `DieModule`, `DamageInfo`, `Thing`, `ModuleData`, `Xfer`, `XferVersion
