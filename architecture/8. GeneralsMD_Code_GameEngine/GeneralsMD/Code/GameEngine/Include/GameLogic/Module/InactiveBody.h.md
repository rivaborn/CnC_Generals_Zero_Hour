# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/InactiveBody.h

## Purpose
Defines the `InactiveBody` module, representing indestructible objects that largely ignore world interactions.

## Responsibilities
- Provides a body module that cannot be damaged or healed
- Overrides damage/healing behavior to do nothing
- Manages basic health and damage state properties
- Supports memory pooling and module system integration

## Key Types
- **InactiveBody (Class)**: Module for indestructible objects.
- **InactiveBodyMagicEnum (Enum)**: Not inferable.
- **InactiveBody_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable.

## Key Functions
### `attemptDamage`
- Purpose: Ignores damage attempts (no-op).
- Calls: None.

### `attemptHealing`
- Purpose: Ignores healing attempts (no-op).
- Calls: None.

### `estimateDamage`
- Purpose: Returns 0 damage (inactive bodies take no damage).
- Calls: None.

### `internalChangeHealth`
- Purpose: Handles internal health changes (empty implementation).
- Calls: None.

## Globals
- None.

## Dependencies
- `BodyModule.h` (inheritance)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
- Module system macros (`MAKE_STANDARD_MODULE_MACRO`)
