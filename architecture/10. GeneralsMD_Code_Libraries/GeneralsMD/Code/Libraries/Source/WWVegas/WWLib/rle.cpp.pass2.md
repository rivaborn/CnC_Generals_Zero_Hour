# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/rle.cpp - Enhanced Analysis

## Architectural Role
This file implements core RLE compression/decompression utilities used throughout the engine for optimizing texture and sprite data storage. The RLEEngine class provides low-level byte manipulation that supports the W3D rendering pipeline's need for efficient memory usage.

## Cross-References
### Incoming
- Likely called by texture/sprite loading systems (e.g., W3D asset handlers)
- Potentially used by map data compression utilities
- May be referenced by network serialization code for efficient data transfer

### Outgoing
- Uses `MIN` macro from `always.h` for run-length limiting
- Relies on standard C++ types and basic memory operations

## Design Patterns
- **Utility Class**: RLEEngine is a stateless utility class with only static methods
- **Data Transformation**: Implements classic RLE compression/decompression algorithm
- **Buffer Management**: Handles pointer arithmetic and length tracking for memory efficiency

*Not inferable*: No clear use of object-oriented patterns beyond basic class structure.
