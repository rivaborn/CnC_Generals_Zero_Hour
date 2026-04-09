# Generals/Code/GameEngine/Source/GameClient/Drawable/Update/SwayClientUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the client-side animation logic for tree sway effects, bridging the game logic (breeze parameters) with the rendering system (drawable transformations). It extends the `ClientUpdateModule` base class to provide per-frame updates for visual wind effects.

## Cross-References
### Incoming
- Called by the game's client update system (likely via `Drawable` or `Thing` update loops)
- Depends on `TheScriptEngine` for breeze parameters and `GameClientRandomValueReal` for randomization

### Outgoing
- Modifies `Drawable` instance matrices directly
- Queries `Object` status bits to determine sway eligibility
- Uses `Xfer` system for network serialization

## Design Patterns
- **Observer Pattern**: Reacts to breeze parameter changes via version tracking
- **State Pattern**: Manages sway enabled/disabled state with `stopSway()`
- **Serialization Pattern**: Uses `xfer` for network synchronization with versioning

*Not inferable*: Exact caller hierarchy or how this integrates with the broader animation system.
