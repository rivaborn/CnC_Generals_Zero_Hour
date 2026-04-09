# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/FireWeaponWhenDamagedBehavior.cpp

## Purpose
Implements behavior for objects to fire weapons when damaged, with different weapons for different damage states.

## Responsibilities
- Manages reaction and continuous weapons for pristine, damaged, really damaged, and rubble states
- Handles damage events to trigger reaction weapons
- Updates continuously to fire weapons based on current damage state
- Serializes/deserializes weapon states for networking
- Manages upgrade activation/deactivation

## Key Types
- **FireWeaponWhenDamagedBehavior (class)**: Main behavior class handling weapon firing logic
- **FireWeaponWhenDamagedBehaviorModuleData (struct)**: Configuration data for the behavior (defined elsewhere)

## Key Functions
### FireWeaponWhenDamagedBehavior()
- Purpose: Constructor that initializes weapons based on module data
- Calls: TheWeaponStore->allocateNewWeapon(), reloadAmmo(), giveSelfUpgrade(), setWakeFrame()

### onDamage()
- Purpose: Handles damage events to trigger appropriate reaction weapons
- Calls: getDamageTypeFlag(), getObject(), getBodyModule(), getDamageState(), forceFireWeapon()

### update()
- Purpose: Continuously fires weapons based on current damage state
- Calls: getObject(), getBodyModule(), getDamageState(), forceFireWeapon()

### crc()
- Purpose: Generates CRC checksum for networking
- Calls: UpdateModule::crc(), UpgradeMux::upgradeMuxCRC()

### xfer()
- Purpose: Serializes/deserializes weapon states for networking
- Calls: UpdateModule::xfer(), UpgradeMux::upgradeMuxXfer(), xferSnapshot()

### loadPostProcess()
- Purpose: Post-processing after loading
- Calls: UpdateModule::loadPostProcess(), UpgradeMux::upgradeMuxLoadPostProcess()

## Globals
- **MAX_IDX (const Int)**: Maximum index value (32)
- **BEGIN_MIDPOINT_RATIO (const Real)**: Ratio for midpoint calculation (0.35f)
- **END_MIDPOINT_RATIO (const Real)**: Ratio for midpoint calculation (0.65f)

## Dependencies
- Common/Thing.h, Common/ThingTemplate.h, Common/INI.h, Common/RandomValue.h, Common/Xfer.h
- GameClient/Drawable.h, GameClient/FXList.h, GameClient/InGameUI.h
- GameLogic/GameLogic.h, GameLogic/Module/BodyModule.h, GameLogic/Module/FireWeaponWhenDamagedBehavior.h
- GameLogic/Module/AIUpdate.h, GameLogic/Object.h, GameLogic/ObjectCreationList.h, GameLogic/Weapon.h
- TheWeaponStore (external symbol)
