# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/texfcach.cpp

## Purpose
Manages texture caching for the game engine, handling storage, retrieval, and compression of texture data.

## Responsibilities
- Cache texture files to disk for faster loading
- Compress/decompress texture data
- Manage in-memory texture surface cache
- Validate and generate texture cache files
- Handle multi-threaded access to texture cache

## Key Types
- `TextureFileCache` (Class): Main texture cache manager
- `Compressor` (Class): Handles texture data compression/decompression
- `FileHeader` (Struct): Stores metadata about cached textures
- `OffsetTableType` (Struct): Tracks offsets/sizes of cached textures

## Key Functions
### `Save_Texture`
- Purpose: Saves texture data to cache file with compression
- Calls: `Open_Texture_Handle`, `Add_Cached_Surface`, `Compressor::Compress`

### `Load_Texture`
- Purpose: Loads texture from cache into surface buffer
- Calls: `Open_Texture_Handle`, `Read_Texture`, `Compressor::Decompress`

### `Validate_Texture`
- Purpose: Ensures texture exists in cache, generating if needed
- Calls: `Texture_Exists`, `Save_Texture`, `Load_Surface`

### `Read_Texture`
- Purpose: Reads compressed texture data from cache file
- Calls: `Compressor::Decompress`

## Globals
- `mutex` (CriticalSectionClass): Thread synchronization
- `compression_buffer` (SimpleVecClass<char>): Buffer for compression operations
- `Instances` (int): Tracks active cache instances

## Dependencies
- `texfcach.h`, `mutex.h`, `thread.h`, `textureloader.h`
- DirectX 8 texture interfaces (`srTextureIFace`, `srColorSurface`)
- File system and compression utilities
