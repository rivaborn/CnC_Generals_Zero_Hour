# GeneralsMD/Code/Libraries/Source/Compression/EAC/refcodex.h - Enhanced Analysis

## Architectural Role
This header defines the REF codec API, a core component of the EAC (Electronic Arts Compression) library used for data compression/decompression across the engine. It serves as the interface for asset compression, particularly for W3D model data and other large binary assets.

## Cross-References
### Incoming
- `GeneralsMD/Code/Libraries/Source/Compression/EAC/codex.c` (implementation)
- `GeneralsMD/Code/Libraries/Source/Compression/EAC/codex.h` (parent include)
- W3D asset loading pipeline (e.g., `GeneralsMD/Code/Libraries/Source/W3D/Loader/w3d_loader.cpp`)

### Outgoing
- None (pure header, no external calls)

## Design Patterns
- **Facade Pattern**: Exposes simplified compression/decompression interface hiding internal REF codec complexity.
- **Dependency Injection**: Requires `codex.h` to be included first, enforcing proper initialization order.
- **Opaque Pointer Pattern**: Uses `void*` for compressed data, allowing internal format changes without breaking callers.
