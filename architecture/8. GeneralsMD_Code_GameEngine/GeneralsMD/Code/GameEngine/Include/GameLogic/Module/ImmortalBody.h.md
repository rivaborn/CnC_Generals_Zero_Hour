# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ImmortalBody.h

## Purpose
Defines the `ImmortalBody` class, a module that extends `ActiveBody` to prevent health from dropping below 1.

## Responsibilities
- Inherits from `ActiveBody` and overrides health modification behavior.
- Ensures the attached object's health never goes below 1.
- Provides memory management and module registration macros.

## Key Types
- **ImmortalBody (Class)**: A body module that prevents health from dropping below 1.
- **ImmortalBodyMagicEnum (Enum)**: Not inferable (likely unused or placeholder).
- **ImmortalBody_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely unused or placeholder).

## Key Functions
### `ImmortalBody(Thing *thing, const ModuleData* moduleData)`
- Purpose: Constructor for `ImmortalBody`.
- Calls: `ActiveBody` constructor (inherited).

### `internalChangeHealth(Real delta)`
- Purpose: Overrides health modification to ensure health never drops below 1.
- Calls: Not inferable (implementation not shown).

## Globals
- None.

## Dependencies
- **Includes**: `GameLogic/Module/ActiveBody.h`
- **External Symbols**: `Object`, `Thing`, `ModuleData`, `Real` (likely from engine core).
