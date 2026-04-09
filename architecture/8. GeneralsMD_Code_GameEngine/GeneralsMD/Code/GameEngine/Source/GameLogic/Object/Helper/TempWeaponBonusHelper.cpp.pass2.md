# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Helper/TempWeaponBonusHelper.cpp - Enhanced Analysis

## Architectural Role
This file implements a helper class for managing temporary weapon bonuses, bridging the gap between game logic (weapon effects) and rendering (visual feedback). It handles the lifecycle of bonuses, including timing, state management, and visual representation.

## Cross-References
### Incoming
- Called by weapon systems when bonuses are applied/removed
- Used by object update loops for expiration handling
- Referenced in save/load serialization

### Outgoing
- Interacts with `Object` for bonus state management
- Modifies `Drawable` for visual effects (tinting)
- Uses `GameLogic` for frame timing

## Design Patterns
- **Observer Pattern**: Wakes up on timer expiration to clear bonuses
- **State Pattern**: Manages different weapon bonus conditions as states
- **Helper Pattern**: Encapsulates bonus logic as a reusable component

*Not inferable*: Exact calling contexts or full dependency graph.
