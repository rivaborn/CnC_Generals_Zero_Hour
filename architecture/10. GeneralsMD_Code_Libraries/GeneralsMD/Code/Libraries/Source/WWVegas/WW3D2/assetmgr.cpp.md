# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/assetmgr.cpp

## Purpose
Manages 3D assets (models, animations, textures, fonts) in the SAGE engine, providing loading, caching, and retrieval functionality.

## Responsibilities
- Load and manage 3D assets from W3D files
- Handle prototype loading via chunk-based system
- Manage texture caching and memory usage
- Provide iterators for asset enumeration
- Track references and memory usage of assets

## Key Types
- `WW3DAssetManager` (Class): Singleton asset manager for 3D resources
- `RObjIterator` (Class): Iterator for render objects
- `HAnimIterator` (Class): Iterator for hierarchical animations
- `HTreeIterator` (Class): Iterator for hierarchy trees
- `Font3DDataIterator` (Class): Iterator for 3D font data
- `PrototypeLoaderClass` (External): Base class for prototype loaders

## Key Functions
### `Load_Procedural_Textures`
- Purpose: Loads procedural textures from metals.ini
- Calls: `MetalManager->Get_Metal_Map()`, `TextureHash.Insert()`

### `Log_Texture_Statistics`
- Purpose: Logs texture memory usage statistics
- Calls: `Log_Textures()`, `Create_Number_String()`

### `Get_Font3DData`
- Purpose: Retrieves or creates Font3DData by name
- Calls: `Add_Font3DData()`

### `Register_Prototype_Loader`
- Purpose: Registers a new prototype loader
- Calls: `PrototypeLoaders.Add()`

### `Find_Prototype_Loader`
- Purpose: Finds loader for a specific chunk type
- Calls: None

### `Add_Prototype`
- Purpose: Adds prototype to hash table and list
- Calls: `Prototypes.Add()`

### `Find_Prototype`
- Purpose: Searches hash table for prototype by name
- Calls: None

## Globals
- `TheInstance` (WW3DAssetManager*): Singleton instance pointer
- `_NullPrototype` (NullPrototypeClass): Special null render object prototype

## Dependencies
- Key includes: `assetmgr.h`, `chunkio.h`, `texture.h`, `font3d.h`, `proto.h`, `hanim.h`, `htree.h`, `shdlib.h`
- External symbols: `WWDEBUG_SAY`, `WWPROFILE`, `NEW_REF`, `W3DNEW`, `W3DNEWARRAY`, `DX8_ErrorCode`
- Windows API: `stricmp`, `memset`
