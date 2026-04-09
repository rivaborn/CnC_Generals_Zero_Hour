# Generals/Code/Libraries/Source/WWVegas/WW3D2/assetmgr.cpp

## Purpose
Manages 3D assets (models, animations, textures, fonts) in the SAGE engine, providing loading, caching, and retrieval functionality.

## Responsibilities
- Loads and caches 3D assets from W3D files
- Manages render objects, HAnims, HTrees, materials, and fonts
- Provides iterators for asset enumeration
- Handles texture caching and memory management
- Registers custom prototype loaders

## Key Types
- **WW3DAssetManager (Class)**: Central asset management singleton
- **RObjIterator (Class)**: Iterates over render objects
- **HAnimIterator (Class)**: Iterates over hierarchical animations
- **HTreeIterator (Class)**: Iterates over hierarchy trees
- **Font3DDataIterator (Class)**: Iterates over 3D font data
- **PrototypeLoaderClass (External)**: Base class for asset loaders

## Key Functions
### Create_Number_String
- Purpose: Formats memory size into human-readable string
- Calls: None

### Log_Textures
- Purpose: Logs texture statistics (count, memory usage, format)
- Calls: `DX8_ErrorCode`, `WWDEBUG_SAY`

### WW3DAssetManager::Get_Font3DData
- Purpose: Retrieves or creates 3D font data
- Calls: `Add_Font3DData`

### WW3DAssetManager::Register_Prototype_Loader
- Purpose: Registers custom asset loaders
- Calls: None

### WW3DAssetManager::Find_Prototype
- Purpose: Locates a prototype by name in hash table
- Calls: `CRC_Stringi`

## Globals
- **TheInstance (WW3DAssetManager*)**: Singleton instance
- **_NullPrototype (NullPrototypeClass)**: Special-case null render object

## Dependencies
- **Headers**: `assetmgr.h`, `chunkio.h`, `texture.h`, `font3d.h`, `proto.h`, `wwstring.h`, `ini.h`
- **External**: `D3D` types, `WWDEBUG`, `WWPROFILE`, `HAnimManagerIterator`, `MetalMapManagerClass`
- **Internal**: `PrototypeLoaderClass`, `RenderObjClass`, `Font3DDataClass`
