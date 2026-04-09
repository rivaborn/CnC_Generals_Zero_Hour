# GeneralsMD/Code/GameEngine/Include/GameLogic/Weapon.h

## Purpose
Defines weapon-related classes, enums, and structures for the game engine, including weapon templates, bonuses, and the weapon store subsystem.

## Responsibilities
- Declares weapon template and runtime weapon classes
- Defines weapon behavior enums (reload types, target masks, etc.)
- Provides weapon bonus system for damage/range modifications
- Manages weapon store subsystem for template lookup

## Key Types
- **WeaponTemplate (Class)**: Template for weapon properties and behavior
- **Weapon (Class)**: Runtime weapon instance with ammo/state tracking
- **WeaponBonus (Class)**: Modifies weapon stats based on conditions
- **WeaponStore (Class)**: Manages weapon templates and delayed damage
- **WeaponReloadType (Enum)**: Auto/No/Return-to-base reload modes
- **WeaponAntiMaskType (Enum)**: Target filtering flags
- **WeaponAffectsMaskType (Enum)**: Damage effect flags
- **WeaponBonusConditionType (Enum)**: Conditions for bonus application

## Key Functions
### WeaponTemplate::fireWeaponTemplate
- Purpose: Fires the weapon template and returns damage frame
- Calls: Not inferable from header

### Weapon::fireWeapon
- Purpose: Fires weapon at target/position
- Calls: privateFireWeapon, reloadWithBonus

### WeaponStore::findWeaponTemplate
- Purpose: Looks up weapon template by name
- Calls: Not inferable from header

## Globals
- **NO_MAX_SHOTS_LIMIT (Int)**: Constant for unlimited shots
- **TheWeaponAffectsMaskNames (char**)**: String names for affect masks
- **TheWeaponStore (WeaponStore**)**: Global weapon store instance

## Dependencies
- Common/AudioEventRTS.h
- GameLogic/Damage.h
- WWMath/Matrix3D.h
- WeaponBonusConditionFlags.h
- WeaponStatus.h
- MemoryPoolObject, Snapshot, INI classes
