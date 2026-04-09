# Generals/Code/Libraries/Source/WWVegas/WWLib/rsacrypt.h - Enhanced Analysis

## Architectural Role
This file implements RSA cryptography for secure key exchange, likely used in the game's networking layer for authentication or secure communications. It bridges the game's custom integer arithmetic library with OpenSSH key formats.

## Cross-References
### Incoming
- Networking subsystem (likely calls `Load_SSH_Keyset` for key loading)
- Authentication/encryption modules (use `Encrypt`/`Decrypt`)

### Outgoing
- `wwlib/int.h` (for large integer operations)
- `wwlib/wwfile.h` (for file I/O)
- XMP_* functions (external modular arithmetic)

## Design Patterns
- **Template Method**: `RSACrypt<PRECISION>` uses template for precision configuration
- **Precomputation**: `Decryption_Setup` caches values for performance
- **Adapter**: Converts OpenSSH key format to internal representation

*Not inferable*: Exact callers of RSA operations in networking layer.
