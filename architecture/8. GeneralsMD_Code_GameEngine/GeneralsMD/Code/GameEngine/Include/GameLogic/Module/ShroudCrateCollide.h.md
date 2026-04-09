# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ShroudCrateCollide.h

## Purpose
Defines a crate collision module that clears shroud (fog of war) for the unit that picks it up.

## Responsibilities
- Inherits from `CrateCollide` to handle crate pickup behavior
- Implements shroud-clearing logic when crate is picked up
- Uses memory pool allocation for performance
- Provides standard module interface (name, CRC, transfer, etc.)

## Key Types
- `ShroudCrateCollide` (Class): Crate collision handler for shroud-clearing behavior
- `ShroudCrateCollideMagicEnum` (Enum): Not inferable (likely internal macro enum)
- `ShroudCrateCollide_GLUE_NOT_IMPLEMENTED` (Enum): Not inferable (likely internal macro enum)

## Key Functions
### `ShroudCrateCollide::ShroudCrateCollide`
- Purpose: Constructor for the shroud-clearing crate collision handler
- Calls: `CrateCollide` constructor

### `ShroudCrateCollide::executeCrateBehavior`
- Purpose: Executes the shroud-clearing behavior when crate is picked up
- Calls: Not inferable (implementation in .cpp file)

## Globals
None

## Dependencies
- `Common/Module.h` (base module class)
- `GameLogic/Module/CrateCollide.h` (base crate collision class)
- `Thing` (forward-declared game object class)
