# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/ArmorUpgrade.cpp

## Purpose
Implements armor upgrades for game objects, modifying their armor properties and visuals.

## Responsibilities
- Applies armor upgrades to objects
- Sets armor flags on the object's body module
- Handles special case for America's chemical suits upgrade
- Implements serialization (Xfer) and CRC for network sync

## Key Types
- **ArmorUpgrade (Class)**: Manages armor upgrades for game objects
- **UpgradeModule (Class)**: Base class for upgrade modules

## Key Functions
### ArmorUpgrade::upgradeImplementation
- Purpose: Applies armor upgrade to the object
- Calls: getObject(), getBodyModule(), setArmorSetFlag(), getDrawable(), setTerrainDecal(), isTriggeredBy()

### ArmorUpgrade::crc
- Purpose: Generates CRC checksum for network synchronization
- Calls: UpgradeModule::crc()

### ArmorUpgrade::xfer
- Purpose: Serializes/deserializes armor upgrade data
- Calls: UpgradeModule::xfer(), xferVersion()

### ArmorUpgrade::loadPostProcess
- Purpose: Post-processing after loading
- Calls: UpgradeModule::loadPostProcess()

## Globals
None

## Dependencies
- Common/Xfer.h
- Common/Player.h
- Common/Upgrade.h
- GameLogic/Object.h
- GameLogic/Module/ArmorUpgrade.h
- GameLogic/Module/BodyModule.h
