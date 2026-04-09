# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/texfcach.h

## Purpose
Header file defining the `TextureFileCache` class for managing texture file caching in the WW3D2 engine.

## Responsibilities
- Manages loading, saving, and caching of texture data
- Handles texture file format and compression
- Provides access to cached texture surfaces
- Validates texture integrity in the cache

## Key Types
- `TextureFileCache` (Class): Manages texture file caching operations
- `FileHeader` (Struct): Contains version information for texture cache files
- `TextureBlockHeader` (Struct): Stores metadata for a cached texture (dimensions, mipmaps, formats)
- `OffsetTableType` (Struct): Tracks file offsets and sizes for cached textures

## Key Functions
### `Texture_Exists`
- Purpose: Checks if a texture exists in the cache
- Calls: None visible

### `Load_Original_Texture_Surface`
- Purpose: Loads the original texture surface without converting texels
- Calls: None visible

### `Save_Texture`
- Purpose: Saves a loaded texture into the file cache
- Calls: None visible

### `Load_Texture`
- Purpose: Loads texture data from cache into a multirequest structure
- Calls: None visible

### `Validate_Texture`
- Purpose: Checks if texture is in cache and loads/saves all mipmap levels if not
- Calls: None visible

### `Get_Surface`
- Purpose: Retrieves a surface from the file cache based on reduction factor
- Calls: None visible

## Globals
- `_FileNamePtr` (char*): Static pointer for creating file names
- `Instances` (int): Static counter for TextureFileCache instances (commented out)

## Dependencies
- `always.h`, `tagblock.h`, `assert.h`
- `FileClass`, `srColorSurfaceIFace`, `srTextureIFace` (forward declarations)
- `TagBlockFile`, `TagBlockHandle` classes
- DX8-specific interfaces (under `WW3D_DX8` guard)
