# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/texture.cpp

## Purpose
Manages texture loading, handling, and memory management in the SAGE engine, including texture invalidation and Direct3D texture operations.

## Responsibilities
- Texture lifecycle management (loading, unloading, invalidation)
- Direct3D texture interface abstraction
- Texture memory optimization (reduction, pooling)
- Texture state tracking (access time, priority)
- Thumbnail and procedural texture support

## Key Types
- **TextureBaseClass (Class)**: Base texture abstraction with D3D texture management
- **TextureClass (Class)**: Extends base with format-specific handling
- **CubeTextureClass (Class)**: Cubemap texture specialization
- **VolumeTextureClass (Class)**: 3D volume texture specialization
- **MipCountType (Enum)**: Mipmap level count options
- **PoolType (Enum)**: Texture memory pool types

## Key Functions
### Load_Texture
- Purpose: Loads texture data from file or generates procedural textures
- Calls: TextureLoader requests, thumbnail loading, D3D texture creation

### setup_texture_attributes
- Purpose: Configures texture filtering and mipmapping settings
- Calls: Filter class methods

### Save_Texture
- Purpose: Saves texture data to file
- Calls: D3D surface locking/access, file I/O

### Invalidate_Old_Unused_Textures
- Purpose: Manages texture memory by unloading unused textures
- Calls: WW3D::Get_Sync_Time(), texture invalidation

### Invalidate
- Purpose: Releases D3D texture resources and marks texture as uninitialized
- Calls: D3DTexture->Release()

## Globals
- **DEFAULT_INACTIVATION_TIME (unsigned)**: Default time before unused textures are unloaded (20000ms)
- **unused_texture_id (unsigned)**: Counter for generating unique texture IDs
- **TexturesAppliedPerFrame (unsigned)**: Tracks texture operations per frame
- **MAX_TEXTURES_APPLIED_PER_FRAME (unsigned)**: Limits texture operations per frame (2)

## Dependencies
- Direct3D 8 headers (d3d8.h, D3dx8core.h)
- WW3D engine components (texture.h, w3d_file.h, assetmgr.h)
- Texture utilities (textureloader.h, missingtexture.h)
- D3D wrapper (dx8wrapper.h, dx8texman.h)
- Profiling (wwprofile.h)
- File format handlers (targa.h, formconv.h)
