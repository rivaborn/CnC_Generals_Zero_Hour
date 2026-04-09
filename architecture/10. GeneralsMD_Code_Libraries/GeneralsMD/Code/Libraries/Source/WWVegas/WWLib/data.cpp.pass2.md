# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/data.cpp - Enhanced Analysis

## Architectural Role
This file serves as the core data loading and resource management layer for the SAGE engine, bridging file I/O, memory allocation, and resource handling. It abstracts platform-specific resource loading (Windows) and provides compression/decompression utilities critical for asset management.

## Cross-References
### Incoming
- **W3D Rendering System**: Uses `Load_Picture` for texture loading
- **UI System**: Calls `Fetch_String` for localized text
- **Asset Pipeline**: Relies on `Hires_Load` for resolution-dependent assets
- **Modding Framework**: Uses `Fetch_Resource` for custom resource loading

### Outgoing
- **File I/O Subsystem**: Directly interacts with `FileClass`
- **Memory Management**: Uses `W3DNEWARRAY` for allocations
- **Windows API**: For resource loading (`FindResource`, etc.)
- **Compression Layer**: Calls `Uncompress_Data`

## Design Patterns
- **Resource Pooling**: `Fetch_String` uses a fixed-size cache (64 entries) with LRU eviction
- **Facade Pattern**: Abstracts platform-specific resource loading behind `Fetch_Resource`
- **Strategy Pattern**: `Load_Uncompress` handles multiple compression formats via header inspection

*Not inferable*: Exact compression algorithm or `CompHeaderType` structure.
