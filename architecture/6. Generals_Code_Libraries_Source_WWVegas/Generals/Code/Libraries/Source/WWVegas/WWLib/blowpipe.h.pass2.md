# Generals/Code/Libraries/Source/WWVegas/WWLib/blowpipe.h - Enhanced Analysis

## Architectural Role
This file implements a streaming encryption/decryption layer using the Blowfish algorithm, fitting into the engine's networking security infrastructure. It extends the `Pipe` abstraction to provide transparent cryptographic processing for data streams, likely used for secure client-server communication.

## Cross-References
### Incoming
- Networking subsystems (e.g., `Generals/Code/Game/Network/`) would use `BlowPipe` for encrypting/decrypting packets
- Modding infrastructure may reference this for custom encryption schemes

### Outgoing
- Directly depends on `BlowfishEngine` (from `blowfish.h`) for cryptographic operations
- Inherits from `Pipe` (from `pipe.h`), implying integration with the engine's data pipeline system

## Design Patterns
- **Decorator Pattern**: `BlowPipe` extends `Pipe` to add encryption/decryption behavior without modifying the base pipe interface
- **Strategy Pattern**: The `CryptControl` enum allows runtime selection of encryption/decryption mode
- **Resource Management**: Uses RAII for `BlowfishEngine` allocation/deallocation in constructor/destructor
