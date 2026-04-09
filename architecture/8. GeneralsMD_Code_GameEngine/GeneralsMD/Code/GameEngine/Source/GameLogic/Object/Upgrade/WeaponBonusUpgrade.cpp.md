# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/WeaponBonusUpgrade.cpp

## Purpose
Implements the WeaponBonusUpgrade module, which applies weapon bonuses to objects via player upgrades.

## Responsibilities
- Constructs/destructs the upgrade module
- Applies weapon bonus conditions to objects
- Handles serialization (CRC, Xfer, loadPostProcess)

## Key Types
- **WeaponBonusUpgrade (Class)**: Manages weapon bonus upgrades for objects
- **UpgradeModule (Base Class)**: Parent class for upgrade modules

## Key Functions
### WeaponBonusUpgrade()
- Purpose: Constructor for WeaponBonusUpgrade
- Calls: UpgradeModule constructor

### ~WeaponBonusUpgrade()
- Purpose: Destructor for WeaponBonusUpgrade
- Calls: None

### upgradeImplementation()
- Purpose: Applies weapon bonus condition to the object
- Calls: getObject(), setWeaponBonusCondition()

### crc()
- Purpose: Serialization CRC function
- Calls: UpgradeModule::crc()

### xfer()
- Purpose: Serialization Xfer function
- Calls: UpgradeModule::xfer(), xfer->xferVersion()

### loadPostProcess()
- Purpose: Post-load processing
- Calls: UpgradeModule::loadPostProcess()

## Globals
None

## Dependencies
- PreRTS.h, Common/Xfer.h, GameLogic/Object.h, GameLogic/Module/WeaponBonusUpgrade.h, GameLogic/Weapon.h
- Xfer class, Thing class, Object class, UpgradeModule class
