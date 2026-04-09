# Generals/Code/Tools/matchbot/wnet/tcp.cpp - Enhanced Analysis

## Architectural Role
This file implements the core TCP networking layer for the matchbot tool, providing cross-platform socket operations with both client and server capabilities. It serves as the foundation for the game's networking infrastructure, handling connection management, data transmission, and error states.

## Cross-References
### Incoming
- `Generals/Code/Tools/mangler/wnet/tcp.cpp` (uses TCP class methods)
- Likely called by matchbot's networking components for actual game matchmaking

### Outgoing
- Directly uses POSIX/Winsock APIs for socket operations
- Relies on `fd_set` macros for connection tracking
- Calls into platform-specific error handling

## Design Patterns
- **Facade Pattern**: Wraps complex socket APIs behind a simple interface
- **State Pattern**: Uses `ConnectionState` enum to track socket state transitions
- **Adapter Pattern**: Abstracts platform differences (Windows/POSIX) behind unified interface

*Not inferable*: No clear use of Observer or Strategy patterns in visible code.
