# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/shapipe.h - Enhanced Analysis

## Architectural Role
This file implements a streaming SHA-1 hash calculator within the engine's pipe system, enabling incremental hash computation for data verification or integrity checks. It bridges the low-level SHA engine with the pipe abstraction layer, likely used for mod file validation or network data integrity.

## Cross-References
### Incoming
- Files using data integrity verification (e.g., mod loading, network packets)
- Systems requiring streaming hash computation (e.g., file I/O, memory buffers)

### Outgoing
- Directly uses `SHAEngine` from `sha.h` for core hashing
- Inherits from `Pipe` for stream processing interface

## Design Patterns
- **Decorator Pattern**: Extends `Pipe` without modifying its interface, adding SHA computation as a side effect
- **Stream Processing**: Processes data incrementally via `Put()`, enabling large-file hashing without loading entire contents
- **Non-copyable**: Private copy constructor/assignment enforces single-ownership semantics for the SHA state
