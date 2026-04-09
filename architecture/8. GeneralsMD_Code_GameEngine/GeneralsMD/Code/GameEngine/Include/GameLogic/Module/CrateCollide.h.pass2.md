# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/CrateCollide.h - Enhanced Analysis

## Architectural Role
This file defines the core abstraction for crate collision behavior, serving as the base class for all crate-related interactions in the game. It bridges the collision detection system with game logic execution, enabling modular crate behaviors like sabotage, healing, or resource drops.

## Cross-References
### Incoming
- **GameLogic/Module/ConvertToCarBombCrateCollide.h**: Overrides `executeCrateBehavior` and `isValidToExecute`.
- **GameLogic/Module/Sabotage*CrateCollide.h**: Multiple sabotage crate types override `executeCrateBehavior` and `isValidToExecute`.
- **GameLogic/Module/MoneyCrateCollide.h**: Overrides `executeCrateBehavior` for resource crates.
- **GameLogic/Module/HealCrateCollide.h**: Implements healing crate behavior.

### Outgoing
- **GameLogic/Module/CollideModule.h**: Inherits from `CollideModule`.
- **FXList**: Uses for feedback effects (`doSabotageFeedbackFX`).
- **Anim2DTemplate**: References for execution animations.

## Design Patterns
- **Template Method**: `executeCrateBehavior` is a pure virtual method, forcing subclasses to implement crate-specific logic while `onCollide` provides the invariant collision handling.
- **Strategy**: Different crate behaviors (sabotage, healing, etc.) are encapsulated in derived classes, allowing dynamic behavior selection via module data.
- **Factory Method**: `buildFieldParse` suggests use of a parsing factory for module data configuration (inferred from `MultiIniFieldParse` usage).
