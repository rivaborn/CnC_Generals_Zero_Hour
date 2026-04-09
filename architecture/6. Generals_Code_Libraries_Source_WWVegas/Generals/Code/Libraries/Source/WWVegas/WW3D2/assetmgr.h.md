# Generals/Code/Libraries/Source/WWVegas/WW3D2/assetmgr.h

## Purpose
Header file defining the WW3DAssetManager class and related asset management infrastructure for the SAGE engine.

## Responsibilities
- Manages 3D assets (meshes, animations, textures, fonts, hierarchy trees)
- Provides loading, creation, and iteration of render objects
- Handles prototype system for custom render object types
- Manages texture caching and metal maps
- Controls load-on-demand behavior for assets

## Key Types
- **WW3DAssetManager (Class)**: Central asset manager for 3D resources
- **AssetIterator (Class)**: Base iterator for asset enumeration
- **RenderObjIterator (Class)**: Iterator for render objects with class ID support
- **PrototypeClass (Class)**: Abstract factory for named render objects
- **PrototypeLoaderClass (Class)**: Importer for W3D chunk types
- **TextureClass (Class)**: Texture resource management
- **Font3DDataClass (Class)**: 3D font data management
- **HTreeClass (Class)**: Hierarchy tree structure
- **HAnimClass (Class)**: Animation data structure

## Key Functions
### Load_3D_Assets
- Purpose: Load 3D assets from file
- Calls: FileClass operations, Load_Prototype

### Create_Render_Obj
- Purpose: Create an instance of a named render object
- Calls: Find_Prototype, PrototypeClass methods

### Get_Texture
- Purpose: Retrieve or load a texture by filename
- Calls: TextureHash operations, TextureFileCache methods

### Register_Prototype_Loader
- Purpose: Add support for custom render object types
- Calls: PrototypeLoaders vector operations

## Globals
- **TheInstance (WW3DAssetManager*)**: Singleton instance of the asset manager
- **WW3D_Load_On_Demand (bool)**: Controls lazy loading behavior
- **Activate_Fog_On_Load (bool)**: Controls fog activation during loading

## Dependencies
- Key includes: "always.h", "vector.h", "htreemgr.h", "hanimmgr.h", "texture.h"
- External symbols: FileClass, PrototypeLoaderClass, TextureClass, etc.
- Uses: DynamicVectorClass, HashTemplateClass, SList, SimpleDynVecClass
