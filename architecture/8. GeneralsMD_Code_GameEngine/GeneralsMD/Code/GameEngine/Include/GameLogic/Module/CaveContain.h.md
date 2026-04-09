# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/CaveContain.h

## Purpose
Defines the `CaveContain` module, a specialized container for cave/tunnel units that manages contained units via `CaveManager`.

## Responsibilities
- Manages cave/tunnel unit containment logic
- Handles team changes across connected caves
- Provides cave-specific containment queries
- Implements distributed garrison behavior

## Key Types
- **CaveContainModuleData (Class)**: Module data with cave index field
- **CaveContain (Class)**: Main cave container class implementing `OpenContain` and `CreateModuleInterface`
- **CaveContainMagicEnum (Enum)**: Not inferable (empty)
- **CaveContain_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty)

## Key Functions
### `CaveContain::tryToSetCaveIndex`
- Purpose: Sets the cave index for grouping caves together
- Calls: Not inferable

### `CaveContain::changeTeamOnAllConnectedCaves`
- Purpose: Propagates team changes to all connected caves
- Calls: Not inferable

### `CaveContain::onDie`
- Purpose: Overrides base die behavior for cave containers
- Calls: Not inferable

## Globals
- None

## Dependencies
- `GameLogic/Module/CreateModule.h`
- `GameLogic/Module/OpenContain.h`
- `Sound` (forward declaration)
- `Team` (forward declaration)
