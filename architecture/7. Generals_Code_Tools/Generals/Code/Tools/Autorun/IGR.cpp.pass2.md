# Generals/Code/Tools/Autorun/IGR.cpp - Enhanced Analysis

## Architectural Role
This file implements the IGR (Internet Game Registry) settings manager, bridging the game's online functionality with Windows registry storage. It serves as the persistence layer for online-related user preferences, particularly for auto-login and nickname storage behaviors.

## Cross-References
### Incoming
- Likely called by online authentication/connection systems (e.g., WOLAPI integration)
- Potentially used by UI components handling login preferences

### Outgoing
- Directly uses Windows Registry API (`RegOpenKeyEx`, `RegQueryValueEx`, etc.)
- Depends on constants defined in `IGR.h` (registry key paths, option flags)

## Design Patterns
- **Registry Adapter Pattern**: Wraps Windows Registry API calls to provide a clean interface for game code
- **Flag Bitmask Pattern**: Uses bitwise operations to manage multiple boolean options in a single integer
- **Singleton-like Global**: While not a true singleton, the global `OnlineOptions` pointer suggests intended single-instance usage

*Not inferable*: No clear use of other patterns like Observer or Factory in this snippet.
