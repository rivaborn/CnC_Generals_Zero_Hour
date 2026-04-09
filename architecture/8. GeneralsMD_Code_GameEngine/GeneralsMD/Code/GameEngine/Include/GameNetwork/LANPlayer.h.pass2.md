# GeneralsMD/Code/GameEngine/Include/GameNetwork/LANPlayer.h - Enhanced Analysis

## Architectural Role
This file defines the `LANPlayer` class, a core component of the LAN networking subsystem. It serves as a data container for player information in the lobby system, bridging the LANAPI and LANGameInfo subsystems.

## Cross-References
### Incoming
- `LANAPI.h` (originally contained this class)
- `LANGameInfo.h` (uses `LANPlayer` for lobby management)
- `GameLobby.h` (likely references `LANPlayer` for player lists)

### Outgoing
- None (pure data class with no external dependencies)

## Design Patterns
- **Data Transfer Object (DTO)**: Encapsulates player data for transfer between networking layers.
- **Linked List Node**: Uses `m_next` pointer to form a linked list of players, common in C++ for dynamic collections.
- **Inline Accessors**: Uses inline getter/setter methods to minimize overhead for frequently accessed fields.
