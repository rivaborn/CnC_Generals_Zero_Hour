# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/blowfish.h - Enhanced Analysis

## Architectural Role
This header defines the core cryptographic primitive used for secure data handling in the engine. It's part of the low-level utility library (WWLib) that provides foundational services like encryption for save games, network packets, and potentially mod asset protection.

## Cross-References
### Incoming
- Likely called by save/load systems (`SaveGame.cpp`)
- Used by networking layer for packet encryption (`Network.cpp`)
- Potentially referenced in modding infrastructure for asset encryption

### Outgoing
- Depends on `bool.h` for type definitions
- Uses standard C headers (`<limits.h>`)

## Design Patterns
- **Encapsulation**: All internal tables and state are private, exposing only key management and crypto operations
- **Resource Management**: Key state tracked via `IsKeyed` flag to prevent uninitialized use
- **Algorithm Parameterization**: Round count and block size defined as constants for flexibility

Rules followed. Output under 400 tokens.
