# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/pkpipe.h - Enhanced Analysis

## Architectural Role
PKPipe implements hybrid encryption for secure data transmission in the SAGE engine's networking layer. It bridges public-key cryptography (PKey) for key exchange and symmetric Blowfish encryption for bulk data, critical for multiplayer game security.

## Cross-References
### Incoming
- Likely called by networking modules (e.g., packet serialization/deserialization)
- Potentially used by save/load systems for encrypted game state

### Outgoing
- Depends on `BlowPipe` for symmetric encryption
- Uses `RandomStraw` for key generation
- Relies on `Pipe` base class for stream processing

## Design Patterns
- **Decorator Pattern**: PKPipe wraps BlowPipe to add encryption/decryption
- **Strategy Pattern**: CryptControl enum selects encryption/decryption behavior
- **State Pattern**: Implicit state machine (IsGettingKey) for key exchange vs. data processing

*Not inferable*: Exact callers or usage context in networking/UI systems.
