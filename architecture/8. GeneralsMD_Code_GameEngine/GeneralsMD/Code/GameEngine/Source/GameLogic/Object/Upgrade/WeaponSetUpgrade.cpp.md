# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/WeaponSetUpgrade.cpp

## Purpose
Implements an upgrade module that flags an object as having a player upgrade, enabling the weapon set chooser to select the appropriate weapon set.

## Responsibilities
- Constructs and destructs the WeaponSetUpgrade module
- Applies the upgrade by setting a weapon set flag on the object
- Handles serialization (CRC, Xfer, loadPostProcess)

## Key Types
- **WeaponSetUpgrade (Class)**: Upgrade module that sets a weapon set bit for the Best Fit weapon set chooser.

## Key Functions
### WeaponSetUpgrade::WeaponSetUpgrade
- Purpose: Constructs the WeaponSetUpgrade module.
- Calls: UpgradeModule constructor

### WeaponSetUpgrade::~WeaponSetUpgrade
- Purpose: Destructs the WeaponSetUpgrade module.
- Calls: None

### WeaponSetUpgrade::upgradeImplementation
- Purpose: Sets the WEAPONSET_PLAYER_UPGRADE flag on the object.
- Calls: getObject(), setWeaponSetFlag()

### WeaponSetUpgrade::crc
- Purpose: Serializes the module for CRC calculation.
- Calls: UpgradeModule::crc()

### WeaponSetUpgrade::xfer
- Purpose: Serializes the module for network transfer.
- Calls: UpgradeModule::xfer(), xfer->xferVersion()

### WeaponSetUpgrade::loadPostProcess
- Purpose: Post-processes the module after loading.
- Calls: UpgradeModule::loadPostProcess()

## Globals
- None

## Dependencies
- PreRTS.h, Common/Xfer.h, GameLogic/Object.h, GameLogic/Module/WeaponSetUpgrade.h
- UpgradeModule, Thing, Object, Xfer, XferVersion, ModuleData, WEAPONSET_PLAYER_UPGRADE
