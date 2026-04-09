# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/srandom.cpp - Enhanced Analysis

## Architectural Role
This file implements the engine's secure random number generation subsystem, critical for game logic requiring unpredictability (e.g., AI decision-making, procedural content). It bridges low-level system entropy sources with the game's RNG needs, using SHA hashing for cryptographic strength while maintaining performance via caching.

## Cross-References
### Incoming
- Likely called by game logic systems needing secure randomness (AI, mission generation)
- Potentially used by networking code for session keys or anti-cheat measures

### Outgoing
- Depends on `SHAEngine` for hashing core functionality
- Uses OS-specific APIs (`GetDiskFreeSpace`, `GetComputerName`) for entropy collection
- Relies on `Random3Class` as a fallback RNG for distribution improvement

## Design Patterns
- **Singleton-like initialization**: The `SecureRandomClass` constructor handles one-time seed generation via static `Initialized` flag
- **Object Pooling**: `RandomCache` pre-generates SHA hashes to amortize cryptographic overhead
- **Hybrid RNG**: Combines SHA output with a simpler RNG (`RandomHelper`) to improve statistical properties

*Not inferable*: Exact callers of `SecureRandomClass` methods remain unclear from this file alone.
