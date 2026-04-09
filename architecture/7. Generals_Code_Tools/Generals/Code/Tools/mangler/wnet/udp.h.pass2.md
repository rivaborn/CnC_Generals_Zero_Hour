# Generals/Code/Tools/mangler/wnet/udp.h - Enhanced Analysis

## Architectural Role
This file provides a cross-platform UDP socket abstraction layer used by network tools (e.g., matchbot, mangler) in the Generals toolchain. It isolates platform-specific socket APIs behind a consistent interface, enabling portable network operations across Windows and Unix-like systems.

## Cross-References
### Incoming
- `Generals/Code/Tools/matchbot/wnet/udp.h` (uses `UDP::Bind`, `UDP::Read`, `UDP::Wait`, `UDP::Write`)
- `Generals/Code/Tools/mangler/wnet/udp.h` (self-references in cross-reference table)

### Outgoing
- Platform-specific socket APIs (`winsock.h`, `sys/socket.h`, etc.)
- `<wlib/wstypes.h>`, `<wlib/wtime.h>` for types and timing utilities

## Design Patterns
- **Adapter Pattern**: Wraps platform-specific socket APIs (Windows/Unix) into a unified interface.
- **Facade Pattern**: Simplifies complex socket operations (binding, I/O, error handling) for toolchain consumers.
- **Error Handling via Enum**: Uses `sockStat` to standardize error codes across platforms.
