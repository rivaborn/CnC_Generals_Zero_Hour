# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Die/UpgradeDie.cpp

## Purpose
Handles removal of an upgrade from a parent object when this object dies.

## Responsibilities
- Removes specified upgrade from parent object on death
- Validates parent object and upgrade existence
- Logs error if upgrade not found on parent

## Key Types
- UpgradeDie (Class): DieModule that removes an upgrade on death
- UpgradeDieModuleData (Not inferable): Module data containing upgrade name

## Key Functions
### UpgradeDie::onDie
- Purpose: Removes upgrade from parent object when this object dies
- Calls: isDieApplicable, TheGameLogic->findObjectByID, TheUpgradeCenter->findUpgrade, producer->hasUpgrade, producer->removeUpgrade

### UpgradeDie::crc
- Purpose: Serialization CRC calculation
- Calls: DieModule::crc

### UpgradeDie::xfer
- Purpose: Serialization/deserialization
- Calls: DieModule::xfer

### UpgradeDie::loadPostProcess
- Purpose: Post-load processing
- Calls: DieModule::loadPostProcess

## Globals
- None

## Dependencies
- PreRTS.h, ThingTemplate.h, Upgrade.h, Xfer.h, Drawable.h, GameLogic.h, UpgradeDie.h, Object.h
- TheGameLogic, TheUpgradeCenter
