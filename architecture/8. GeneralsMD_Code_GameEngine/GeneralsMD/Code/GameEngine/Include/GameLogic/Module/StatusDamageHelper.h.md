# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/StatusDamageHelper.h

## Purpose
Header for a game module that manages clearing status conditions (e.g., damage effects) on objects over time.

## Responsibilities
- Manages timed removal of status effects from game objects
- Provides interface for applying and clearing status conditions
- Handles periodic updates to check if status effects should expire
- Integrates with the game's module and memory management systems

## Key Types
- **StatusDamageHelperModuleData (Class)**: Module data container (empty implementation)
- **StatusDamageHelper (Class)**: Main helper class for managing status condition timers
- **StatusDamageHelperMagicEnum (Enum)**: Not inferable (likely macro-related)
- **StatusDamageHelper_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely macro-related)

## Key Functions
### `StatusDamageHelper()`
- Purpose: Constructor for the StatusDamageHelper
- Calls: Not inferable

### `update()`
- Purpose: Periodically checks if status conditions should be cleared
- Calls: Not inferable

### `doStatusDamage()`
- Purpose: Applies a status effect with a specified duration
- Calls: Not inferable

### `clearStatusCondition()`
- Purpose: Removes the current status condition from the object
- Calls: Not inferable

## Globals
- None

## Dependencies
- `GameLogic/Module/ObjectHelper.h`
- `ModuleData` (base class)
- `ObjectHelper` (base class)
- `Thing` (game object type)
- `DisabledMaskType`, `DISABLEDMASK_ALL` (update control)
- `ObjectStatusTypes` (status effect types)
- `Real`, `UnsignedInt` (primitive types)
- Memory pool macros (`MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`, `MEMORY
