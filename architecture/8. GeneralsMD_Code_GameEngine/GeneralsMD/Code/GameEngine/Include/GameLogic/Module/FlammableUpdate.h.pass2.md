# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/FlammableUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the flammability system for objects in the game, integrating with the damage and update module frameworks. It handles state transitions (normal/aflame/burned) and their effects, including damage application and audio feedback.

## Cross-References
### Incoming
- **DamageModule**: Calls `onDamage()` when objects take damage
- **UpdateModule**: Calls `update()` for periodic state management
- **FlammableDamage**: Likely calls `tryToIgnite()` to initiate burning

### Outgoing
- **AudioSystem**: Uses `AudioHandle` for burning sound playback
- **DamageModuleInterface**: Implements damage handling for aflame states
- **UpdateModule**: Inherits update timing and sleep logic

## Design Patterns
- **Module Pattern**: Extends `UpdateModule` and `DamageModuleInterface` for composable behavior
- **State Machine**: Manages flammability states (normal/aflame/burned) with time-based transitions
- **Observer**: Reacts to damage events via `onDamage()` for dynamic behavior

*Not inferable: Exact audio event handling or flame damage limit mechanics.*
