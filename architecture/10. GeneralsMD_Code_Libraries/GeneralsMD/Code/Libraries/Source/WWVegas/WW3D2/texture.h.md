# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/texture.h

## Purpose
Defines texture-related classes and interfaces for the SAGE engine, including regular, cube, and volume textures, as well as Direct3D texture wrappers.

## Responsibilities
- Abstracts Direct3D texture types (2D, cube, volume)
- Manages texture loading, initialization, and memory usage
- Provides texture filtering and mipmapping support
- Handles texture prioritization and invalidation
- Supports serialization for W3D file I/O

## Key Types
- **TextureBaseClass (Class)**: Base class for all texture types, handling common functionality like loading, memory management, and Direct3D integration.
- **TextureClass (Class)**: Represents standard 2D textures with format and filtering support.
- **ZTextureClass (Class)**: Specialized texture for depth/stencil buffers.
- **CubeTextureClass (Class)**: Handles cube map textures for environment mapping.
- **VolumeTextureClass (Class)**: Manages 3D volume textures.
- **PoolType (Enum)**: Defines memory pool types (default, managed, system memory).
- **TexAssetType (Enum)**: Classifies texture types (regular, cubemap, volume).

## Key Functions
### `Apply_New_Surface`
- Purpose: Updates texture surface data after loading.
- Calls: Not inferable (virtual function, implementation in derived classes).

### `Apply`
- Purpose: Applies texture settings to a Direct3D stage.
- Calls: Not inferable (virtual function, implementation in derived classes).

### `Load_Texture`
- Purpose: Loads a texture from a W3D file chunk.
- Calls: Not inferable (declared but not defined in header).

### `Save_Texture`
- Purpose: Saves a texture to a W3D file chunk.
- Calls: Not inferable (declared but not defined in header).

## Globals
None.

## Dependencies
- Direct3D 8 interfaces (`IDirect3DBaseTexture8`, etc.)
- Engine-specific classes (`SurfaceClass`, `TextureFilterClass`, `RefCountClass`)
- W3D file I/O (`ChunkLoadClass`, `ChunkSaveClass`)
- Utility types (`StringClass`, `Vector3`, `WW3DFormat`)
