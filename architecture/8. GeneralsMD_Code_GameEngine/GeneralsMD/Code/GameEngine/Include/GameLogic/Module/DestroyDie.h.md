# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/DestroyDie.h

## Purpose
Defines the `DestroyDie` module, a default implementation for handling object destruction in the game.

## Responsibilities
- Implements the `DieModule` interface for object destruction logic.
- Handles the `onDie` event when an object is destroyed.
- Provides memory management macros for object pooling.
- Exposes standard module macros for registration and serialization.

## Key Types
- **DestroyDie (Class)**: Default die module handling object destruction.
- **DestroyDieMagicEnum (Enum)**: Not inferable (likely unused or placeholder).
- **DestroyDie_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely unused or placeholder).

## Key Functions
### `DestroyDie(Thing *thing, const ModuleData* moduleData)`
- Purpose: Constructor for the `DestroyDie` module.
- Calls: Not inferable (constructor body not shown).

### `onDie(const DamageInfo *damageInfo)`
- Purpose: Handles the destruction logic when an object dies.
- Calls: Not inferable (implementation not shown).

## Globals
- None

## Dependencies
- `DieModule.h` (base class)
- `INI.h` (for configuration)
- `Thing` (forward-declared, likely game entity class)
