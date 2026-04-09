# Generals/Code/Libraries/Source/WWVegas/WW3D2/texfcach.h

## Purpose
Header file for the TextureFileCache class, managing texture file caching for the WW3D2 engine.

## Responsibilities
- Defines the TextureFileCache class for texture caching
- Declares file format structures for texture storage
- Provides interface for texture loading/saving operations
- Manages cached texture surfaces and file handles

## Key Types
- **TextureFileCache (Class)**: Manages texture file caching operations
- **FileHeader (Struct)**: Contains version information for cache files
- **TextureBlockHeader (Struct)**: Stores metadata for individual textures
- **OffsetTableType (Struct)**: Tracks file offsets and sizes for textures

## Key Functions
### TextureFileCache(const char *fileprefix)
- Purpose: Constructor for TextureFileCache
- Calls: Not inferable

### Load_Original_Texture_Surface(const char *texturename)
- Purpose: Loads original texture surface without converting texels
- Calls: Not inferable

### Save_Texture(const char *texturename, srTextureIFace::MultiRequest& mreq, srColorSurfaceIFace& origsurface)
- Purpose: Saves texture data to file cache
- Calls: Not inferable

### Load_Texture(const char *texturename, srTextureIFace::MultiRequest& mreq)
- Purpose: Loads texture data from cache into multirequest structure
- Calls: Not inferable

### Validate_Texture(const char* texturename)
- Purpose: Checks if texture exists in cache and loads all mipmap levels if not
- Calls: Not inferable

## Globals
- **_FileNamePtr (char*)**: Static pointer for file name creation

## Dependencies
- `always.h`, `tagblock.h`
- `FileClass`, `srColorSurfaceIFace`, `srTextureIFace` (forward declarations)
- `assert.h` for debugging assertions
