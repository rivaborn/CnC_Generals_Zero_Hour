# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/CrateCollide.cpp - Enhanced Analysis

## Architectural Role
This file implements the base collision logic for supply crates, serving as the foundation for all crate-related interactions in the game. It handles pickup validation, effect triggering, and sabotage feedback, acting as a central point for crate behavior that is extended by specialized crate types.

## Cross-References
### Incoming
- Multiple specialized crate collision classes (e.g., `MoneyCrateCollide`, `VeterancyCrateCollide`) inherit and override behavior from this base class.
- `ConvertToHijackedVehicleCrateCollide` and other conversion crate types use this as their parent class.

### Outgoing
- Calls into `FXList` for visual effects, `InGameUI` for animations, and `GameAudio` for sound feedback.
- Relies on `GameLogic` for object destruction and `Player` for ownership checks.

## Design Patterns
- **Template Method Pattern**: `executeCrateBehavior` is declared virtual, allowing derived classes to implement specific crate behaviors while maintaining a consistent interface.
- **Strategy Pattern**: The `CrateCollideModuleData` class encapsulates configuration data (pickup rules, effects) that can be swapped out for different crate types.
- **Observer Pattern**: The `onCollide` method acts as an event handler for collision events, triggering appropriate responses.

Rules followed. Output under 400 tokens.
