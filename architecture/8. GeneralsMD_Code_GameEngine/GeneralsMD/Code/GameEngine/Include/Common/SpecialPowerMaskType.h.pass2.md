# GeneralsMD/Code/GameEngine/Include/Common/SpecialPowerMaskType.h - Enhanced Analysis

## Architectural Role
This header defines the bitmask type used to track which special powers (e.g., superweapons, abilities) are active or available in the game. It serves as a foundational type for power state management across game logic and networking subsystems.

## Cross-References
### Incoming
- Game logic files (e.g., `Unit.cpp`, `Building.cpp`) use this type to track unit/building power states
- Networking code (`Replication.cpp`) likely serializes power masks for multiplayer sync
- UI/HUD systems (`HUD.cpp`) may use it to display power cooldowns/availability

### Outgoing
- Relies on `BitFlags.h`/`BitFlagsIO.h` for bitmask operations and serialization
- Depends on `SpecialPowerType.h` for the underlying enum defining power types

## Design Patterns
- **Type Aliasing**: Uses `typedef` to create a domain-specific bitmask type for clarity
- **Header-Only**: Pure declaration file to avoid compilation dependencies
- **Bitmask Pattern**: Encapsulates power state as a set of flags for efficient storage/operations

*Not inferable*: No runtime patterns visible from header alone.
