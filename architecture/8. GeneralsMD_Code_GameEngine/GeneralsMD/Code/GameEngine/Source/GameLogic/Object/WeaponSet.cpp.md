# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/WeaponSet.cpp

## Purpose
Manages weapon sets for game objects, including weapon selection, targeting, and state management.

## Responsibilities
- Weapon template set parsing and management
- Weapon selection logic for targets
- Weapon state tracking (locking, reloading, ammo)
- Damage type and anti-mask calculations

## Key Types
- `WeaponTemplateSet` (Class): Manages weapon templates and their properties
- `WeaponSet` (Class): Handles weapon selection and state for game objects
- `WeaponSetFlags` (Struct): Bit flags for weapon set conditions
- `WeaponSlotType` (Enum): Weapon slot identifiers (PRIMARY, SECONDARY, etc.)

## Key Functions
### `getVictimAntiMask`
- Purpose: Determines anti-mask for a target based on its kind
- Calls: `victim->isKindOf()` checks for various target types

### `chooseBestWeaponForTarget`
- Purpose: Selects optimal weapon for a target based on criteria
- Calls: `weapon->estimateWeaponDamage()`, `weapon->isWithinTargetPitch()`, `getVictimAntiMask()`

### `updateWeaponSet`
- Purpose: Updates weapon set based on object template
- Calls: `TheWeaponStore->allocateNewWeapon()`, `weapon->loadAmmoNow()`

### `setWeaponLock`/`releaseWeaponLock`
- Purpose: Manages weapon locking/unlocking
- Calls: None (state management only)

## Globals
- `WeaponSetFlags::s_bitNameList` (const char*): Weapon flag names for parsing

## Dependencies
- `WeaponSet.h`, `Weapon.h`, `INI.h`, `ThingFactory.h`
- `Object.h`, `AI.h`, `ContainModule.h`
- `TheWeaponStore`, `TheThingFactory` global instances
