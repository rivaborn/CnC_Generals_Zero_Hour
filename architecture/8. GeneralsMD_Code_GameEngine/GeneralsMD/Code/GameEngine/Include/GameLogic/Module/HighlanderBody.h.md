# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/HighlanderBody.h

## Purpose
Defines the HighlanderBody class, a module for objects that take damage but cannot die from normal damage.

## Responsibilities
- Inherits from ActiveBody to provide damage handling.
- Overrides attemptDamage to implement special damage logic.
- Uses memory pool allocation for performance.
- Implements standard module macros for game engine integration.

## Key Types
- **HighlanderBody (Class)**: Body module that resists normal damage but can die from unresistible damage.
- **HighlanderBodyMagicEnum (Enum)**: Not inferable (likely unused placeholder).
- **HighlanderBody_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely unused placeholder).

## Key Functions
### HighlanderBody()
- Purpose: Constructor for HighlanderBody.
- Calls: Not inferable (constructor body not shown).

### attemptDamage()
- Purpose: Handles damage attempts with special logic for Highlander objects.
- Calls: Not inferable (implementation not shown).

## Globals
None

## Dependencies
- **ActiveBody.h**: Base class for body modules.
- **Object**: Forward-declared class reference.
- **ModuleData**: Used in constructor (not shown in header).
