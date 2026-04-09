# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/HealCrateCollide.h

## Purpose
Defines a crate collision module that heals objects owned by the colliding entity.

## Responsibilities
- Inherits from `CrateCollide` to handle crate collision behavior
- Implements healing logic for owned objects
- Manages memory allocation via custom memory pool
- Provides module interface for game engine integration

## Key Types
- **HealCrateCollide (Class)**: Crate collision module that heals owned objects
- **HealCrateCollideMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **HealCrateCollide_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### HealCrateCollide()
- Purpose: Constructor for the heal crate collision module
- Calls: `CrateCollide` parent constructor

### executeCrateBehavior()
- Purpose: Executes the healing behavior when crate is collided with
- Calls: Not inferable (implementation in .cpp file)

## Globals
- None

## Dependencies
- `Common/Module.h` (base module class)
- `GameLogic/Module/CrateCollide.h` (parent class)
- `Thing` (forward-declared class reference)
