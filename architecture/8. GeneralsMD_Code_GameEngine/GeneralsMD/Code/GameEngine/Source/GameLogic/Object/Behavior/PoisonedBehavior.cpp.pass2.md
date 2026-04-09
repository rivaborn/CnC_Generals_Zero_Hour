# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/PoisonedBehavior.cpp - Enhanced Analysis

## Architectural Role
This file implements the poison state machine for game objects, bridging the damage system and visual effects. It's part of the behavior module system that extends object functionality through composition.

## Cross-References
### Incoming
- Damage system calls `onDamage()` when poison damage occurs
- Healing system calls `onHealing()` to clear poison state
- Update system calls `update()` for periodic damage application

### Outgoing
- Calls `Drawable::setTintStatus()` for visual poison effects
- Uses `GameLogic::getFrame()` for timing calculations
- Invokes `Object::attemptDamage()` for periodic damage

## Design Patterns
- **State Pattern**: Manages poisoned/non-poisoned states with clear entry/exit points
- **Module Pattern**: Extends base `UpdateModule` for composable behavior
- **Time-based Processing**: Uses frame counters for damage intervals and duration

*Not inferable*: Exact relationship with damage type system or how poison interacts with other status effects.
