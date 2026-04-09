# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SpecialAbility.h

## Purpose
Defines the `SpecialAbility` class for handling special attacks from units in the game.

## Responsibilities
- Inherits from `SpecialPowerModule` to implement special attack logic.
- Provides virtual methods for executing special powers at objects, locations, or generally.
- Uses memory pool management and module data macros for object lifecycle.

## Key Types
- **SpecialAbilityModuleData (Class)**: Module data for `SpecialAbility`.
- **SpecialAbility (Class)**: Core class for special attack processing.
- **SpecialAbilityMagicEnum (Enum)**: Not inferable (likely unused placeholder).
- **SpecialAbility_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely unused placeholder).

## Key Functions
### `SpecialAbility(Thing *thing, const ModuleData *moduleData)`
- Purpose: Constructor for `SpecialAbility`.
- Calls: Not inferable (constructor body not shown).

### `doSpecialPowerAtObject(Object *obj, UnsignedInt commandOptions)`
- Purpose: Executes special power on a target object.
- Calls: Not inferable (implementation not shown).

### `doSpecialPowerAtLocation(const Coord3D *loc, Real angle, UnsignedInt commandOptions)`
- Purpose: Executes special power at a world location.
- Calls: Not inferable (implementation not shown).

### `doSpecialPower(UnsignedInt commandOptions)`
- Purpose: Executes special power without a specific target.
- Calls: Not inferable (implementation not shown).

## Globals
None.

## Dependencies
- **Includes**: `GameLogic/Module/SpecialPowerModule.h`
- **Forward References**: `Object`
- **Macros**: `MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`, `MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`
