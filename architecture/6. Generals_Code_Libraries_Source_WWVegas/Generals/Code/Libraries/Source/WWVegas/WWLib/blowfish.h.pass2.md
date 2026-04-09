# Generals/Code/Libraries/Source/WWVegas/WWLib/blowfish.h - Enhanced Analysis

## Architectural Role
This header defines the core cryptographic primitive used for secure data handling in the engine, likely for protecting save games, network packets, or mod assets. Its placement in WWLib suggests it's part of the foundational utilities layer.

## Cross-References
### Incoming
- Not inferable from header alone (implementation would show callers)

### Outgoing
- Depends on `bool.h` for type definitions
- Uses `<limits.h>` for `UCHAR_MAX`

## Design Patterns
- **Template Method**: `Process_Block` defines the algorithm skeleton while `Sub_Key_Encrypt` implements the core transformation
- **Resource Management**: `IsKeyed` flag enforces proper key initialization before operations
- **Data Hiding**: Internal tables (`P_Encrypt`, `bf_S`) are private, exposing only the public interface

*Not inferable*: No clear use of Singleton or Factory patterns visible in header.
