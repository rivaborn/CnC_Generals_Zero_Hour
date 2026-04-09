# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ConvertToHijackedVehicleCrateCollide.h - Enhanced Analysis

## Architectural Role
This file defines a specialized crate collision module that implements the "terrorist" crate behavior, converting target vehicles to hijacked state. It extends the base crate collision system, integrating with the game's object interaction and side-switching mechanics.

## Cross-References
### Incoming
- Likely called by the crate drop system when a terrorist crate collides with a vehicle
- Used by the game's side-switching logic to validate and execute hijacking

### Outgoing
- Inherits from `CrateCollide`, calling its base methods
- Interacts with `Thing` objects for collision detection
- Uses `ModuleData` pattern for configuration

## Design Patterns
- **Template Method**: `executeCrateBehavior()` defines the algorithm skeleton for crate behavior
- **Strategy**: Implements a specific strategy for crate collision effects
- **Inheritance**: Extends `CrateCollide` to specialize behavior

*Not inferable: Exact interaction with side-switching system or driver killing mechanics*
