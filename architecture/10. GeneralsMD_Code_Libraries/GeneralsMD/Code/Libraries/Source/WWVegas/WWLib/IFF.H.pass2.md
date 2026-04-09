# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/IFF.H - Enhanced Analysis

## Architectural Role
This header bridges the engine's file I/O layer with its asset loading pipeline, exposing IFF/LBM format handling and compression utilities. It serves as the central interface for managing game assets (textures, models) in a platform-agnostic way, with tight coupling to assembly-optimized routines for performance-critical operations.

## Cross-References
### Incoming
- **Asset Loading**: `Load_Data`, `Load_Uncompress` called by resource managers (e.g., texture, model loaders).
- **Rendering**: `Load_Picture` used by W3D renderer for texture loading.
- **Modding**: Exposed to modding infrastructure for custom asset handling.

### Outgoing
- **File I/O**: Direct system calls (not abstracted).
- **Assembly**: `LCW_Compress/Uncompress`, `Pack_2_Plane` for low-level optimizations.
- **Buffer Management**: `BufferClass` for memory handling.

## Design Patterns
- **Facade Pattern**: Hides complexity of IFF/LBM formats behind simple APIs.
- **Strategy Pattern**: Compression methods (LCW, LZW) are interchangeable via `CompressionType`.
- **Adapter Pattern**: Converts between byte-per-pixel and bitplane formats for legacy compatibility.
