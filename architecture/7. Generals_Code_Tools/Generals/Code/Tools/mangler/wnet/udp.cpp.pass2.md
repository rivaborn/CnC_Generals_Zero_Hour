# Generals/Code/Tools/mangler/wnet/udp.cpp - Enhanced Analysis

## Architectural Role
This file implements a cross-platform UDP socket abstraction layer used by the game's networking tools (mangler and matchbot). It provides a consistent interface for UDP operations across Windows and Unix-like systems, isolating platform-specific socket APIs.

## Cross-References
### Incoming
- `Generals/Code/Tools/matchbot/wnet/udp.cpp` (uses UDP class methods)
- `Generals/Code/Tools/mangler/wnet/udp.cpp` (self-references in cross-reference table)

### Outgoing
- POSIX socket API (`socket`, `bind`, `sendto`, `recvfrom`, `select`)
- Windows Sockets API (`ioctlsocket`, `WSAGetLastError`)
- Standard C library (`gethostbyname`, `inet_addr`, `errno`)
- `wlib/wdebug.h` for debugging utilities

## Design Patterns
- **Facade Pattern**: Wraps platform-specific socket APIs behind a unified interface
- **Adapter Pattern**: Converts between host/port representations (network byte order vs host byte order)
- **Strategy Pattern**: Different implementations for Windows vs Unix blocking mode control

*Not inferable*: No clear use of Observer, Factory, or other patterns in this file.
