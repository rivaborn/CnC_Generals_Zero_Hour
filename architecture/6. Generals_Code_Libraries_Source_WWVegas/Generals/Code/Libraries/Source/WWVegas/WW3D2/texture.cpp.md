# Generals/Code/Libraries/Source/WWVegas/WW3D2/texture.cpp

## Purpose
Manages texture loading, rendering, and memory usage in the SAGE engine's 3D graphics subsystem.

## Responsibilities
- Texture creation/loading from files or surfaces
- Memory management and usage tracking
- Filtering and mipmapping configuration
- Bumpmap generation
- Serialization/deserialization of textures

## Key Types
- **TextureClass (Class)**: Core texture wrapper handling Direct3D textures
- **BumpmapTextureClass (Class)**: Specialized texture for bump mapping
- **FilterType (Enum)**: Texture filtering modes (NONE, FAST, BEST, DEFAULT)
- **MipCountType (Enum)**: Mipmap level counts (MIP_LEVELS_1, MIP_LEVELS_2, etc.)
- **PoolType (Enum)**: Memory pool types (POOL_DEFAULT, POOL_MANAGED, POOL_SYSTEMMEM)

## Key Functions
### Calculate_Texture_Memory_Usage
- Purpose: Computes memory usage of a texture across all mip levels
- Calls: `Peek_DX8_Texture()`, `GetLevelDesc()`

### Load_Texture
- Purpose: Loads texture from a chunk file
- Calls: `WW3DAssetManager::Get_Texture()`, `WW3DAssetManager::Get_Bumpmap_Based_On_Texture()`

### setup_texture_attributes
- Purpose: Configures texture attributes for serialization
- Calls: `Get_Mip_Mapping()`, `Get_U_Addr_Mode()`, `Get_V_Addr_Mode()`

### Save_Texture
- Purpose: Serializes texture to a chunk file
- Calls: `Get_Full_Path()`, `setup_texture_attributes()`

## Globals
- **unused_texture_id (unsigned)**: Auto-incrementing ID counter for textures
- **_MinTextureFilters (unsigned[4])**: Minification filter settings per quality level
- **_MagTextureFilters (unsigned[4])**: Magnification filter settings per quality level
- **_MipMapFilters (unsigned[4])**: Mipmap filter settings per quality level

## Dependencies
- Direct3D 8 headers (`d3d8.h`, `D3dx8core.h`)
- Engine-specific headers (`texture.h`, `dx8wrapper.h`, `assetmgr.h`)
- File I/O (`w3d_file.h`, `targa.h`)
- Memory management (`nstrdup.h`)
