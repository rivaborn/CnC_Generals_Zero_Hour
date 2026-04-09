# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Die/FXListDie.cpp

## Purpose
Handles death effects for game objects using FXList (effects list) module.

## Responsibilities
- Manages death effects playback when an object dies
- Checks upgrade activation and conflicts before playing effects
- Supports orientation of effects toward the damage source
- Handles serialization (Xfer) and CRC for network sync

## Key Types
- **FXListDie (Class)**: Die module that plays FXList effects on object death
- **FXListDieModuleData (Struct)**: Not inferable (defined elsewhere)

## Key Functions
### FXListDie::onDie
- Purpose: Plays death effects when object dies, if upgrade is active and no conflicts exist
- Calls: `isUpgradeActive`, `isDieApplicable`, `getUpgradeActivationMasks`, `FXList::doFXObj`, `FXList::doFXPos`

### FXListDie::crc
- Purpose: Serializes module data for CRC calculation
- Calls: `DieModule::crc`

### FXListDie::xfer
- Purpose: Serializes module data for network sync
- Calls: `DieModule::xfer`

### FXListDie::loadPostProcess
- Purpose: Post-load initialization
- Calls: `DieModule::loadPostProcess`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/INI.h`, `Common/Player.h`, `Common/ThingTemplate.h`, `Common/Xfer.h`, `GameClient/FXList.h`, `GameLogic/Damage.h`, `GameLogic/GameLogic.h`, `GameLogic/Object.h`, `GameLogic/Module/FXListDie.h`, `GameLogic/Module/AIUpdate.h`
- `DieModule`, `FXList`, `TheGameLogic`, `UpgradeMaskType
