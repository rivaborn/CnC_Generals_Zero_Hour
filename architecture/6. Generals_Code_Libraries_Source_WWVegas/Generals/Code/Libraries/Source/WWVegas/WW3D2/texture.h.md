# Generals/Code/Libraries/Source/WWVegas/WW3D2/texture.h

## Purpose
Defines the `TextureClass` and related types for texture management in the SAGE engine, including Direct3D texture handling, filtering, and memory management.

## Responsibilities
- Manages Direct3D texture objects and their properties (filtering, addressing, mipmaps).
- Provides texture loading/saving via W3D file I/O.
- Tracks texture memory usage and priority for resource management.
- Supports procedural bumpmap generation.
- Handles texture state application to D3D pipeline stages.

## Key Types
- **TextureClass (Class)**: Core texture wrapper with D3D texture, filtering, and addressing modes.
- **PoolType (Enum)**: Texture memory pool type (default, managed, system memory).
- **FilterType (Enum)**: Texture filtering modes (none, fast, best, default).
- **TxtAddrMode (Enum)**: Texture addressing modes (repeat, clamp).
- **MipCountType (Enum)**: Mipmap level counts (1â12 levels or all).
- **BumpmapTextureClass (Class)**: Procedural bumpmap texture generator.

## Key Functions
### `Load_Texture`
- Purpose: Loads a texture from a W3D file chunk.
- Calls: `ChunkLoadClass` methods (not visible in header).

### `Save_Texture`
- Purpose: Saves a texture to a W3D file chunk.
- Calls: `ChunkSaveClass` methods (not visible in header).

## Globals
- None.

## Dependencies
- `DX8Wrapper`, `IDirect3DTexture8`, `TextureLoader`, `LoaderThreadClass`, `DX8TextureManagerClass`, `TextureLoadTaskClass` (forward declarations).
- `always.h`, `refcount.h`, `chunkio.h`, `surfaceclass.h`, `ww3dformat.h`, `wwstring.h`.
