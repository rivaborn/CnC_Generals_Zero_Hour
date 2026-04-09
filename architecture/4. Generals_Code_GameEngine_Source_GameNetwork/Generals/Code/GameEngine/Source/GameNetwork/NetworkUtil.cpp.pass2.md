# Generals/Code/GameEngine/Source/GameNetwork/NetworkUtil.cpp - Enhanced Analysis

## Architectural Role
This file serves as the central utility layer for network command processing in the SAGE engine, bridging low-level networking (IP resolution) with high-level game synchronization logic. It enforces command routing policies (ACK requirements, synchronization flags) that govern the deterministic lockstep model critical for multiplayer consistency.

## Cross-References
### Incoming
- `GameNetwork/NetworkMsg.cpp` (uses command classification functions)
- `GameNetwork/NetworkPlayer.cpp` (relies on command ID generation)
- `GameNetwork/NetworkRouter.cpp` (consults routing policies)
- `GameNetwork/NetworkGame.cpp` (uses frame synchronization utilities)

### Outgoing
- POSIX networking (`gethostbyname`, `inet_addr`)
- Engine logging (`DEBUG_LOG`)
- `AsciiString` utility class

## Design Patterns
- **Strategy Pattern**: Command classification functions (`DoesCommandRequireACommandID`, `CommandRequiresAck`) act as predicates that delegate routing decisions to other subsystems.
- **Singleton-like Behavior**: `GenerateNextCommandID` uses a static counter, though not a formal singleton, demonstrating lightweight state management for command sequencing.
- **Type Mapping**: `GetAsciiNetCommandType` implements a classic enum-to-string mapping pattern for debugging and serialization.

*Not inferable*: No clear use of Observer or Factory patterns in this utility layer.
