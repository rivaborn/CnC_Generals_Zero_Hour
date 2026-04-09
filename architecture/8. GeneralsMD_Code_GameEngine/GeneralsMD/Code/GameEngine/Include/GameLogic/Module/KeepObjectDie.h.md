# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/KeepObjectDie.h

## Purpose
Defines a die module for objects that should leave rubble when destroyed but lack other die modules.

## Responsibilities
- Inherits from `DieModule` to handle object destruction.
- Implements `onDie` to manage rubble placement.
- Uses memory pooling for object management.
- Provides standard module macros for registration.

## Key Types
- `KeepObjectDie` (Class): Die module for rubble-generating objects.
- `KeepObjectDieMagicEnum` (Enum): Not inferable (likely unused).
- `KeepObjectDie_GLUE_NOT_IMPLEMENTED` (Enum): Not inferable (likely unused).

## Key Functions
### `KeepObjectDie(Thing *thing, const ModuleData* moduleData)`
- Purpose: Constructor for the die module.
- Calls: Not inferable (likely initializes base class).

### `onDie(const DamageInfo *damageInfo)`
- Purpose: Handles object destruction and rubble placement.
- Calls: Not inferable (likely calls base class or rubble logic).

## Globals
- None

## Dependencies
- `DieModule.h` (base class)
- `INI.h` (for module data)
- `Thing` (forward-declared object class)
