# GeneralsMD/Code/GameEngine/Include/GameLogic/WeaponSet.h

## Purpose
Defines classes and enums for weapon management in the game, including weapon sets, templates, and attack logic.

## Responsibilities
- Declares `WeaponSet`, `WeaponTemplateSet`, and related enums for weapon behavior.
- Manages weapon selection, locking, and attack feasibility.
- Handles weapon state transitions (firing, reloading, etc.).
- Provides interfaces for weapon template parsing and condition checking.

## Key Types
- **WeaponSet (Class)**: Manages a unit's weapon configuration and state.
- **WeaponTemplateSet (Class)**: Holds weapon templates and their properties.
- **WeaponSetConditionType (Enum)**: Represents weapon state conditions (firing, reloading, etc.).
- **WeaponChoiceCriteria (Enum)**: Criteria for selecting weapons (damage, range).
- **WeaponLockType (Enum)**: Lock states for weapons (not locked, temporary, permanent).
- **CanAttackResult (Enum)**: Result of attack feasibility checks.

## Key Functions
### `WeaponSet::chooseBestWeaponForTarget`
- Purpose: Selects the optimal weapon for a target based on criteria.
- Calls: Not inferable (implementation in .cpp).

### `WeaponSet::getAbleToUseWeaponAgainstTarget`
- Purpose: Checks if a weapon can be used against a specific target.
- Calls: Not inferable.

### `WeaponSet::updateWeaponSet`
- Purpose: Updates the weapon set state (e.g., reloading, ammo checks).
- Calls: Not inferable.

## Globals
- **TheWeaponSetTypeToModelConditionTypeMap (Array)**: Maps weapon set types to model conditions.
- **TheWeaponSlotTypeNames (Array)**: Names for weapon slots (PRIMARY, SECONDARY, etc.).

## Dependencies
- `INI`, `Object`, `Weapon`, `WeaponTemplate` (forward declarations).
- `CommandSourceType`, `DamageType` (enums from other modules).
- `Snapshot`, `SparseMatchFinder` (base classes/utilities).
- `WeaponSetType.h`, `WeaponSetFlags.h` (included headers).
