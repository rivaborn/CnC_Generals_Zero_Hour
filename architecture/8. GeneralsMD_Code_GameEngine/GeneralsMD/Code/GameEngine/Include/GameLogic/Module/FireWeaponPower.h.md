# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/FireWeaponPower.h

## Purpose
Defines the `FireWeaponPower` module for firing a specific weapon controlled by a superweapon timer.

## Responsibilities
- Inherits from `SpecialPowerModule` to handle weapon firing logic.
- Manages module data via `FireWeaponPowerModuleData`.
- Implements virtual methods for executing special powers at locations or objects.
- Uses memory pool macros for object management.

## Key Types
- **FireWeaponPowerModuleData (Class)**: Holds module-specific data (e.g., `m_maxShotsToFire`).
- **FireWeaponPower (Class)**: Core class for firing weapons as a special power.
- **FireWeaponPowerMagicEnum (Enum)**: Not inferable (likely internal macro enum).
- **FireWeaponPower_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable.

## Key Functions
### `FireWeaponPowerModuleData::buildFieldParse`
- Purpose: Registers module data fields for parsing.
- Calls: `MultiIniFieldParse` methods.

### `FireWeaponPower::doSpecialPower`
- Purpose: Executes the special power with given command options.
- Calls: Not inferable (virtual override).

### `FireWeaponPower::doSpecialPowerAtLocation`
- Purpose: Fires the weapon at a specific location and angle.
- Calls: Not inferable.

### `FireWeaponPower::doSpecialPowerAtObject`
- Purpose: Fires the weapon at a target object.
- Calls: Not inferable.

## Globals
- None.

## Dependencies
- `SpecialPowerModule.h` (base class).
- `Object`, `SpecialPowerTemplate`, `FieldParse`, `ScienceType` (forward declarations).
- Memory pool and module macros (internal SAGE engine).
