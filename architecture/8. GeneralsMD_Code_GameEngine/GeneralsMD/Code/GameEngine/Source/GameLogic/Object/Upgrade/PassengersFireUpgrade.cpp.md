# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/PassengersFireUpgrade.cpp

## Purpose
Implements the PassengersFireUpgrade module, which enables passengers in a container to fire weapons.

## Responsibilities
- Constructs and destructs the upgrade module
- Applies the upgrade to allow passengers to fire
- Handles serialization (Xfer) and CRC for save/load
- Performs post-load processing

## Key Types
- **PassengersFireUpgrade (Class)**: Upgrade module enabling passenger fire permissions
- **ContainModuleInterface (Interface)**: Used to set passenger fire flag

## Key Functions
### PassengersFireUpgrade()
- Purpose: Constructor for the upgrade module
- Calls: UpgradeModule constructor

### ~PassengersFireUpgrade()
- Purpose: Destructor for the upgrade module
- Calls: None

### upgradeImplementation()
- Purpose: Applies the upgrade to enable passenger firing
- Calls: getObject(), getContain(), setPassengerAllowedToFire()

### crc()
- Purpose: Serialization CRC calculation
- Calls: UpgradeModule::crc()

### xfer()
- Purpose: Serialization/deserialization handler
- Calls: UpgradeModule::xfer(), xferVersion()

### loadPostProcess()
- Purpose: Post-load processing
- Calls: UpgradeModule::loadPostProcess()

## Globals
- None

## Dependencies
- PreRTS.h, Common/Xfer.h, GameLogic/Object.h, PassengersFireUpgrade.h, ContainModule.h
- UpgradeModule, Thing, Object, ContainModuleInterface, Xfer, XferVersion
