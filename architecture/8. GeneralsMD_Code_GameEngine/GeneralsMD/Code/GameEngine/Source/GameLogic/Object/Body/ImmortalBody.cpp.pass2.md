# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Body/ImmortalBody.cpp - Enhanced Analysis

## Architectural Role
This file implements a specialized body module that enforces invulnerability by preventing health from dropping below 1. It integrates into the game's damage system and object lifecycle, ensuring certain objects (like player bases or scripted entities) cannot be destroyed.

## Cross-References
### Incoming
- Damage system calls `internalChangeHealth` when applying damage
- Object lifecycle calls `loadPostProcess` during initialization
- Network synchronization calls `crc` and `xfer` for state replication

### Outgoing
- Extends `ActiveBody` functionality for core health management
- Uses `Xfer` for serialization/deserialization
- Relies on `Thing` and `Object` base classes for game entity integration

## Design Patterns
- **Template Method**: Extends `ActiveBody` while overriding specific behavior (health modification)
- **Decorator**: Adds invulnerability behavior without modifying core damage logic
- **Strategy**: Health modification can be swapped via module system (not inferable if other body types exist)
