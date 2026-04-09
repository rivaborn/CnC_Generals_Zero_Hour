# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/rsacrypt.h - Enhanced Analysis

## Architectural Role
This file implements RSA cryptography for secure key exchange and data encryption, critical for the game's networking layer. It bridges the game's custom integer arithmetic (Int class) with external multiprecision math (XMP functions), enabling secure communications in multiplayer.

## Cross-References
### Incoming
- Likely called by networking modules (e.g., `GeneralsMD/Code/Game/Network`) for encrypting/decrypting game data or authentication.
- Potentially used by modding tools for secure asset validation.

### Outgoing
- Depends on `wwlib/int.h` for large integer operations.
- Uses `XMP_Prepare_Modulus`/`XMP_Mod_Mult` (external) for optimized modular arithmetic.
- Relies on `FileClass` (from `wwfile.h`) for SSH key file I/O.

## Design Patterns
- **Template Method**: Uses `template <int PRECISION>` to allow flexible integer precision.
- **Precomputation**: `Decryption_Setup()` caches values (e.g., `DmodPm1`, `RP`) to optimize decryption via the Chinese Remainder Theorem.
- **Facade**: Wraps complex RSA math (e.g., modular exponentiation) behind simple `Encrypt`/`Decrypt` methods.

*Not inferable*: No clear use of Singleton or Observer patterns.
