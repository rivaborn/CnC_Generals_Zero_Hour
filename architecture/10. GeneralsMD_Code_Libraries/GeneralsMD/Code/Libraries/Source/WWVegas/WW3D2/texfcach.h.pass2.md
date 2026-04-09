# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/texfcach.h - Enhanced Analysis

## Architectural Role
This header defines the `TextureFileCache` class, a critical component in the WW3D2 rendering pipeline. It manages texture caching, compression, and mipmapping, serving as an intermediary between the file system and the GPU texture management system (`srTextureIFace`). Its role is to optimize texture loading by persisting processed textures to disk and reusing them across game sessions.

## Cross-References
### Incoming
- Likely called by rendering subsystems (e.g., material/shader loading) and asset managers.
- `srTextureIFace` implementations would use this for texture data retrieval.

### Outgoing
- Depends on `TagBlockFile` for file I/O abstraction.
- Interfaces with `srColorSurfaceIFace` for surface manipulation.
- Uses `FileClass` for low-level file operations (commented in header).

## Design Patterns
- **Resource Pool Pattern**: Manages a pool of cached texture surfaces (`CachedSurfaces` array) with LRU-like eviction (`Find_Smallest_Cached_Surface`).
- **Facade Pattern**: Abstracts texture file format details (headers, offsets) behind a clean API.
- **Singleton-like Behavior**: Static `Instances` counter (commented) suggests intended singleton management for static resources.

*Not inferable*: Exact compression strategy or thread-safety mechanisms.
