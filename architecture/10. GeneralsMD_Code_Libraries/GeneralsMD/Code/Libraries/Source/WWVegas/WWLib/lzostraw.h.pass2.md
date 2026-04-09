# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/lzostraw.h - Enhanced Analysis

## Architectural Role
This file defines the `LZOStraw` class, which is part of the data streaming pipeline in the SAGE engine. It handles LZO compression/decompression for data streams, fitting into the broader I/O and resource management subsystem.

## Cross-References
### Incoming
- Likely called by resource loading systems (e.g., W3D model loading, texture streaming)
- May be used by save/load game functionality for compressed data storage

### Outgoing
- Inherits from `Straw` (base class for data streaming)
- Uses LZO compression library (external dependency)

## Design Patterns
- **Decorator Pattern**: Extends `Straw` base class to add compression/decompression behavior
- **Strategy Pattern**: `CompControl` enum allows runtime selection of compression/decompression mode
- **Resource Management**: Internal buffers (`Buffer`, `Buffer2`) are managed manually (no RAII)
