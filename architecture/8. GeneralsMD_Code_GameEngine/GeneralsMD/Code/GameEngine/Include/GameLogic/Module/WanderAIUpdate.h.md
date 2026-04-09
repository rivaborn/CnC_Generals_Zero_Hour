# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/WanderAIUpdate.h

## Purpose
Defines the `WanderAIUpdate` class, which implements random movement behavior for soldiers in the game.

## Responsibilities
- Implements random movement logic for AI-controlled units.
- Extends `AIUpdateInterface` to customize soldier behavior.
- Provides state machine creation for AI control.
- Manages memory allocation via `MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`.

## Key Types
- **WanderAIUpdate (Class)**: AI behavior module for random movement.
- **WanderAIUpdateMagicEnum (Enum)**: Not inferable (likely unused).
- **WanderAIUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely unused).

## Key Functions
### `update()`
- Purpose: Handles periodic AI updates for random movement.
- Calls: Not inferable (implementation in `.cpp` file).

### `WanderAIUpdate(Thing*, const ModuleData*)`
- Purpose: Constructor for the `WanderAIUpdate` class.
- Calls: Not inferable.

### `makeStateMachine()`
- Purpose: Creates the AI state machine for movement logic.
- Calls: Not inferable.

## Globals
- None.

## Dependencies
- `AIUpdate.h` (base class `AIUpdateInterface`).
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`, `MAKE_STANDARD_MODULE_MACRO`).
