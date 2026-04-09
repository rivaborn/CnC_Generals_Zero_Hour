# Generals/Code/Libraries/Source/WWVegas/WW3D2/texturefile.cpp

## Purpose
Manages texture loading, caching, and reduction for the WW3D2 rendering system.

## Responsibilities
- Loads and caches textures from files
- Manages texture reduction (mipmapping) for performance
- Tracks texture memory usage and locked surfaces
- Provides debug features like texture flashing

## Key Types
- **TextureFileClass (Class)**: Main texture management class
- **MultiRequest (Struct)**: Holds multiple LOD (Level of Detail) surfaces
- **TextureLoaderInfo (Struct)**: Stores texture loading parameters

## Key Functions
### `TextureFileClass::getMipmapData`
- Purpose: Fills a MultiRequest with texture data at appropriate LODs
- Calls: `Fill_Multi_Request_From_Surface`, `Load_Temp_Surface`, `Release_Temp_Surface`, `Process_Reduction`

### `TextureFileClass::Process_Reduction`
- Purpose: Adjusts texture resolution based on current needs
- Calls: `invalidate`, `TextureLoader::Add_Load_Task`

### `TextureFileClass::Load_Locked_Surface`
- Purpose: Loads a high-priority texture that stays in memory
- Calls: `TextureLoader::Load_Locked_Surface_Immediate`

### `TextureFileClass::Update_Texture_Flash`
- Purpose: Handles debug texture flashing effect
- Calls: `WW3D::Get_Sync_Time`

## Globals
- **head (TextureFileClass*)**: Linked list of all texture files
- **mipmaps (bool)**: Global mipmapping enable flag
- **texture_count (int)**: Total number of textures loaded
- **locked_surface_count (int)**: Number of locked surfaces
- **texture_id (int)**: Auto-incrementing ID counter

## Dependencies
- `texturefile.h`, `textureloader.h`, `ww3d.h`, `wwstring.h`
- `rawfile.h`, `ffactory.h`, `nstrdup.h`, `texfcach.h`, `assetmgr.h`
- DirectX 8 headers (`srCore.hpp`, `srSurfaceIOManager.hpp`)
- `texture.h` for TextureFileClass inheritance
