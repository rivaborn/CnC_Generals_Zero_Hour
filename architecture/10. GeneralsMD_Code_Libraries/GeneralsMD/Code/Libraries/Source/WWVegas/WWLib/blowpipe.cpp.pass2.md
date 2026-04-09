# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/blowpipe.cpp - Enhanced Analysis

## Architectural Role
This file implements a cryptographic pipeline layer for secure data transmission in the SAGE engine, bridging the networking subsystem with the Blowfish encryption engine. It handles stream-based encryption/decryption with partial block buffering, critical for secure multiplayer communication.

## Cross-References
### Incoming
- Networking subsystem (likely calls `BlowPipe::Put` for encrypting outgoing packets)
- Modding infrastructure (potential calls to `BlowPipe::Key` for custom encryption keys)

### Outgoing
- `Pipe` base class (for chaining cryptographic operations)
- `BlowfishEngine` (for actual encryption/decryption)
- Memory management (`new` for engine instantiation)

## Design Patterns
- **Pipeline Pattern**: Chains cryptographic operations through `Pipe` inheritance
- **Buffering Pattern**: Manages partial blocks for stream processing efficiency
- **Lazy Initialization**: Creates `BlowfishEngine` only when first key is submitted

*Not inferable*: Exact callers from networking/UI subsystems not visible in this file.
