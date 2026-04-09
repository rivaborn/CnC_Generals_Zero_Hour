# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/FlammableUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the flame state management system for game objects, bridging the damage system, audio subsystem, and object status updates. It handles the temporal aspects of burning (ignition, duration, damage) and coordinates with other update modules like FireSpreadUpdate.

## Cross-References
### Incoming
- Damage system calls `onDamage()` when flame/particle beam damage occurs
- Object status queries check `OBJECT_STATUS_AFLAME`/`OBJECT_STATUS_BURNED` flags
- FireSpreadUpdate references this module for ignition coordination

### Outgoing
- Calls into `BodyModule` for visual aflame state
- Uses `GameAudio` for burning sound effects
- Queries `GameLogic` for frame timing
- Interfaces with `FireSpreadUpdate` for fire propagation

## Design Patterns
- **State Pattern**: Manages object flame states (normal/aflame/burned) with clear transitions
- **Observer Pattern**: Reacts to damage events via `onDamage()` callback
- **Timer-Based Updates**: Uses frame-based timers for flame duration/damage application
