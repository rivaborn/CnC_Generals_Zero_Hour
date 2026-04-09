# Generals/Code/Libraries/Source/WWVegas/WW3D2/texture.h - Enhanced Analysis

## Architectural Role
This file defines the core texture abstraction in the SAGE engine, bridging Direct3D texture management with higher-level game systems. It handles texture loading, memory management, and rendering state application, serving as the central interface for all texture-related operations in the engine.

## Cross-References
### Incoming
- `missingtexture.h` uses `Load_Texture` and `Save_Texture` for fallback texture handling
- Likely called by rendering subsystems (e.g., material/shader systems) to apply textures to D3D stages

### Outgoing
- Depends on `DX8Wrapper` for Direct3D device interaction
- Uses `TextureLoader` and `LoaderThreadClass` for asynchronous texture loading
- Interacts with `DX8TextureManagerClass` for resource management
- Relies on `ChunkLoadClass`/`ChunkSaveClass` for W3D file I/O

## Design Patterns
- **Facade Pattern**: `TextureClass` abstracts Direct3D texture complexity behind a simpler interface
- **Resource Pooling**: Uses `PoolType` to manage texture memory allocation strategies
- **Observer Pattern**: Background loader notifies textures via `Apply_New_Surface` callback

*Not inferable*: Exact threading model for `LoaderThreadClass` or memory management strategies.
