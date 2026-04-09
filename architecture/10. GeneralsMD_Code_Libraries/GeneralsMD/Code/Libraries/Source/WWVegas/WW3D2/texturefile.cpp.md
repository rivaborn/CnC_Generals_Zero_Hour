# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/texturefile.cpp

## Purpose
Manages texture loading, caching, and dynamic resolution scaling for the WW3D rendering engine.

## Responsibilities
- Loads and caches texture surfaces from files
- Handles dynamic texture resolution reduction for performance
- Tracks texture memory usage and locked surface counts
- Provides debug visualization tools (flashing textures)
- Manages texture frame handles and mipmap generation

## Key Types
- **TextureFileClass (Class)**: Main texture management class handling loading, caching, and resolution scaling
- **MultiRequest (Struct)**: Container for multi-level-of-detail texture requests
- **texture_loader_info (Struct)**: Holds loading parameters and callbacks

## Key Functions
### `getMipmapData(MultiRequest& m)`
- Purpose: Fills a multi-level texture request with surface data
- Calls: `Fill_Multi_Request_From_Surface`, `Load_Temp_Surface`, `Release_Temp_Surface`, `Process_Reduction`

### `Process_Reduction()`
- Purpose: Adjusts texture resolution based on current vs desired reduction factor
- Calls: `invalidate`, `TextureLoader::Add_Load_Task`

### `Load_Locked_Surface()`
- Purpose: Loads a high-priority texture surface that stays in memory
- Calls: `TextureLoader::Load_Locked_Surface_Immediate`

### `Update_Texture_Flash()`
- Purpose: Updates debug flashing textures
- Calls: `invalidateFrameHandle`, `Release_Temp_Surface`

## Globals
- **head (TextureFileClass*)**: Linked list head of all texture files
- **mipmaps (bool)**: Global mipmapping enable flag
- **texture_count (int)**: Total number of loaded textures
- **locked_surface_count (int)**: Count of locked (always-in-memory) textures
- **texture_id (int)**: Auto-incrementing ID counter for textures

## Dependencies
- `texturefile.h`, `textureloader.h`, `ww3d.h`, `wwstring.h`
- `rawfile.h`, `ffactory.h`, `nstrdup.h`, `texfcach.h`, `assetmgr.h`
- DirectX 8 headers (`srCore.hpp`, `srSurfaceIOManager.hpp`)
- `texture.h` for base texture interface
