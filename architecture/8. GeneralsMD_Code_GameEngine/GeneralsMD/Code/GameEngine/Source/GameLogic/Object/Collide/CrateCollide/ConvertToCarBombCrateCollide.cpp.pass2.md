# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/ConvertToCarBombCrateCollide.cpp - Enhanced Analysis

## Architectural Role
This file implements the specific collision behavior for "Convert to Car Bomb" crates, extending the base `CrateCollide` class. It bridges the game's crate system with unit conversion mechanics, AI goal tracking, and visual/audio effects, ensuring proper synchronization across networked games.

## Cross-References
### Incoming
- **AIUpdate.h**: Uses `AIUpdateInterface` to verify the unit is the AI's current goal (prevents accidental conversions).
- **FXList.h**: Triggers visual/audio effects (`doFXObj`) during conversion.
- **ExperienceTracker.h**: Transfers veterancy levels from the terrorist to the converted unit.
- **Radar.h**: Updates radar visibility for the converted unit (`removeObject`/`addObject`).

### Outgoing
- **CrateCollide.cpp**: Inherits core crate collision logic.
- **ScriptEngine.h**: Transfers object names for script control.
- **Object.h**: Manages unit status, weapon sets, and ownership changes.

## Design Patterns
- **Template Method**: Extends `CrateCollide` with specialized `isValidToExecute` and `executeCrateBehavior` implementations.
- **Strategy**: Encapsulates car bomb conversion as a modular behavior that can be attached to different crate types.
- **Observer**: Indirectly notifies `TheRadar` of unit visibility changes post-conversion.

*Not inferable*: No clear use of Factory, Visitor, or Decorator patterns.
