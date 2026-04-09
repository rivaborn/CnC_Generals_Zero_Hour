# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SubdualDamageHelper.h

## Purpose
Header for a game module that manages subdual damage and healing for game objects.

## Responsibilities
- Handles subdual damage state for objects
- Manages healing process for subdued objects
- Provides notification for subdual damage events
- Implements standard module interface

## Key Types
- **SubdualDamageHelperModuleData (Class)**: Module data container (empty implementation)
- **SubdualDamageHelper (Class)**: Main helper class for subdual damage management
- **SubdualDamageHelperMagicEnum (Enum)**: Not inferable (likely macro-related)
- **SubdualDamageHelper_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely macro-related)

## Key Functions
### SubdualDamageHelper::update
- Purpose: Handles periodic updates for subdual healing
- Calls: Not inferable

### SubdualDamageHelper::notifySubdualDamage
- Purpose: Notifies the helper about subdual damage events
- Calls: Not inferable

## Globals
- None

## Dependencies
- `GameLogic/Module/ObjectHelper.h`
- `ModuleData` (base class)
- `ObjectHelper` (base class)
- `Thing` (parameter type)
- `DisabledMaskType`, `DISABLEDMASK_ALL` (types for update control)
- `UpdateSleepTime` (return type)
- `Real` (parameter type)
- `UnsignedInt` (member variable type)
- Memory pool macros (`MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA`, `MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
