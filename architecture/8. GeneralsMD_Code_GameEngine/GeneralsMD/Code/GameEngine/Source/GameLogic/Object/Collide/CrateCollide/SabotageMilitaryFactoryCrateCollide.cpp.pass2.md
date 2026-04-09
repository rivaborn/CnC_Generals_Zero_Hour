# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/SabotageMilitaryFactoryCrateCollide.cpp - Enhanced Analysis

## Architectural Role
This file implements the sabotage behavior for military factory crates, extending the base `CrateCollide` class. It integrates with the game's collision system, AI targeting, and feedback effects, acting as a specialized collision handler for terrorist sabotage mechanics.

## Cross-References
### Incoming
- Called by AI modules (e.g., `HijackerUpdate`, `SabotageMilitaryFactoryCrateCollide`) during collision resolution
- Used by `Object` instances when processing collision events

### Outgoing
- Calls `CrateCollide` base class methods for shared crate behavior
- Interacts with `Radar` for infiltration events and `Eva` for announcements
- Uses `AIUpdateInterface` to verify target validity

## Design Patterns
- **Template Method**: Extends `CrateCollide` with specialized sabotage logic while reusing base behavior
- **Strategy**: Encapsulates sabotage behavior as a module, allowing dynamic assignment to objects
- **Observer**: Triggers radar and EVA notifications as side effects of sabotage execution
