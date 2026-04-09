# Generals/Code/Tools/matchbot/wnet/tcp.h - Enhanced Analysis

## Architectural Role
This file provides a cross-platform TCP socket abstraction used by matchbot tooling for network operations. It bridges low-level OS socket APIs with higher-level networking logic, enabling both client and server modes with configurable blocking behavior.

## Cross-References
### Incoming
- `Generals/Code/Tools/mangler/wnet/tcp.h` (duplicate file in another tool)
- Likely called by matchbot's networking components (not explicitly listed)

### Outgoing
- Uses `wlib/wstypes.h`, `wlib/wdebug.h`, `wlib/wtime.h` for Westwood's utility types
- Platform-specific includes for Windows (`winsock.h`) and Unix (`sys/socket.h`)

## Design Patterns
- **Facade Pattern**: Wraps platform-specific socket APIs behind a unified interface
- **State Pattern**: Uses `ConnectionState` enum to track connection lifecycle
- **Strategy Pattern**: Implicit in `Wait()` methods where different timeout strategies can be applied

*Not inferable*: Exact implementation details of async operations or error recovery.
