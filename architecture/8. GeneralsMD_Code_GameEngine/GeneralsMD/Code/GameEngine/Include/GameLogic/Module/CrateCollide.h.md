# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/CrateCollide.h

## Purpose
Defines the abstract base class for crate collision behavior in the game, handling interactions when crates collide with objects.

## Responsibilities
- Declares the `CrateCollide` abstract class and its data structure.
- Defines collision validation and execution logic.
- Provides sabotage feedback effects.
- Manages module data for crate behavior configuration.

## Key Types
- **CrateCollideModuleData (Class)**: Holds configuration data for crate collision behavior.
- **CrateCollide (Class)**: Abstract base class for crate collision logic.
- **SabotageVictimType (Enum)**: Types of buildings that can be sabotaged.

## Key Functions
### `onCollide`
- Purpose: Handles collision events between crates and other objects.
- Calls: `wouldLikeToCollideWith`, `executeCrateBehavior`.

### `executeCrateBehavior`
- Purpose: Abstract method for derived classes to implement crate-specific behavior.
- Calls: None (pure virtual).

### `isValidToExecute`
- Purpose: Checks if a collision is valid for execution.
- Calls: None.

### `doSabotageFeedbackFX`
- Purpose: Plays feedback effects for sabotage actions.
- Calls: None.

## Globals
- None.

## Dependencies
- `CollideModule.h`
- `Thing`, `Anim2DTemplate`, `FXList`, `ScienceType` (forward declarations).
