# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/pk.cpp - Enhanced Analysis

## Architectural Role
This file implements the core public-key cryptography subsystem for the SAGE engine, handling key generation, encryption, and decryption. It serves as the foundation for secure networking operations in multiplayer gameplay, including matchmaking and data integrity verification.

## Cross-References
### Incoming
- Networking subsystem (likely `net.cpp`) calls `PKey::Encrypt`/`Decrypt` for secure packet transmission
- Save/load system (possibly `savegame.cpp`) uses `PKey::Encode_Modulus`/`Decode_Modulus` for protected storage
- Modding infrastructure (e.g., `mod.cpp`) may reference key generation for custom encryption schemes

### Outgoing
- Directly uses `BigInt` class for modular arithmetic operations
- Depends on `Straw` (random number generator) for cryptographic randomness
- Interfaces with DER encoding/decoding utilities (external to this file)

## Design Patterns
- **Template Method**: Key generation process follows a fixed algorithmic sequence
- **Facade**: Hides complex RSA operations behind simple encrypt/decrypt interfaces
- **Strategy**: Different exponent handling for "fast" vs "slow" keys (65537 vs custom)

*Not inferable*: Exact relationship with networking protocol stack or error handling mechanisms.
