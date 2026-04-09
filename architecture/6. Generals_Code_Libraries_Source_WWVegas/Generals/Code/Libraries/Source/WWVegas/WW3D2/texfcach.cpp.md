# Generals/Code/Libraries/Source/WWVegas/WW3D2/texfcach.cpp

## Purpose
Manages texture caching for the game, storing and retrieving compressed texture data to/from disk.

## Responsibilities
- Compresses and stores textures in a cache file
- Loads and decompresses textures from cache
- Manages in-memory cache of recently used textures
- Validates texture existence and generates cache entries
- Handles thread-safe access to texture cache

## Key Types
- `TextureFileCache` (Class): Main texture cache manager
- `Compressor` (Class): Handles texture compression/decompression
- `FileHeader` (Struct): Stores metadata about cached textures
- `OffsetTableType` (Struct): Tracks offsets/sizes of cached textures

## Key Functions
### `Save_Texture`
- Purpose: Compresses and stores a texture in the cache file
- Calls: `Open_Texture_Handle`, `Add_Cached_Surface`, `Compressor::Compress`

### `Load_Texture`
- Purpose: Loads and decompresses a texture from cache
- Calls: `Open_Texture_Handle`, `Read_Texture`, `Compressor::Decompress`

### `Validate_Texture`
- Purpose: Ensures a texture exists in cache, generating it if needed
- Calls: `Texture_Exists`, `Save_Texture`

### `Read_Texture`
- Purpose: Reads compressed texture data from cache file
- Calls: `Compressor::Decompress`

## Globals
- `mutex` (CriticalSectionClass): Thread synchronization
- `compression_buffer` (SimpleVecClass<char>): Buffer for compression operations
- `Instances` (int): Tracks active cache instances

## Dependencies
- `texfcach.h`, `mutex.h`, `thread.h`, `textureloader.h`
- DirectX 8 texture interfaces (`srColorSurfaceIFace`, `srTextureIFace`)
- File system utilities (`FileClass`, `TagBlockHandle`)
- Compression utilities (internal `Compressor` class)
