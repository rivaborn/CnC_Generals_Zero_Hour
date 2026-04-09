# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/PropagandaCenterBehavior.cpp - Enhanced Analysis

## Architectural Role
This file implements the propaganda center's brainwashing mechanics, extending the prison behavior system. It handles unit conversion logic, state tracking, and network synchronization for the propaganda center's unique functionality.

## Cross-References
### Incoming
- Called by prison behavior system when units are captured/removed
- Used by game logic during object updates and network synchronization

### Outgoing
- Extends `PrisonBehavior` functionality
- Interacts with `TheGameLogic` for object lookup and frame tracking
- Uses `Xfer` system for serialization
- Modifies `Object` team ownership and surrender status

## Design Patterns
- **Template Method**: Extends base prison behavior with specialized brainwashing logic
- **State Tracking**: Maintains brainwashing progress via frame counting
- **Resource Management**: Explicit cleanup of brainwashed units in `onDelete`

Rules followed. Analysis limited to 400 tokens.
