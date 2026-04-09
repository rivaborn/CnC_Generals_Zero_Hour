# Generals/Code/Tools/mangler/wnet/tcp.h - Enhanced Analysis

## Architectural Role
This file defines the core TCP networking abstraction used across the engine for both client and server communication. It sits between the platform-specific socket APIs and higher-level networking systems like matchmaking and game state synchronization.

## Cross-References
### Incoming
- `Generals/Code/Tools/matchbot/wnet/tcp.h` uses `TCP::Connect`, `TCP::Read`, `TCP::Wait`, and `TCP::Write` for matchmaking server communication
- Other networking tools likely depend on this for basic socket operations

### Outgoing
- Uses WLib utilities (`wstypes.h`, `wdebug.h`, `wtime.h`) for cross-platform types, debugging, and timing
- Directly interfaces with platform socket APIs (winsock/unix sockets)

## Design Patterns
- **Facade Pattern**: Wraps platform-specific socket APIs behind a unified interface
- **State Pattern**: Uses `ConnectionState` enum to track connection lifecycle (CLOSED/CONNECTING/CONNECTED)
- **Error Handling**: Custom error codes (OK, CONNREFUSED, etc.) abstract platform-specific error values

*Not inferable*: No clear use of other patterns like Singleton or Observer in this header.
