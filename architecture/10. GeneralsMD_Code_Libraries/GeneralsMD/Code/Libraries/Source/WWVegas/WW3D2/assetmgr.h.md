# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/assetmgr.h

## Purpose
Header file defining the WW3D asset management system, including the WW3DAssetManager class and related iterator classes for handling 3D assets like models, animations, textures, and fonts.

## Responsibilities
- Manages loading, creation, and iteration of 3D assets
- Handles prototype systems for render objects
- Provides access to textures, animations, hierarchy trees, and fonts
- Implements asset caching and reference management

## Key Types
- **WW3DAssetManager (Class)**: Central asset manager for 3D resources
- **AssetIterator (Class)**: Base iterator for asset enumeration
- **RenderObjIterator (Class)**: Iterator for render objects with class ID support
- **PrototypeClass (Class)**: Abstract factory for named render objects
- **PrototypeLoaderClass (Class)**: Imports W3D chunks into prototypes
- **TextureClass (Class)**: Texture resource management
- **HAnimClass (Class)**: Hierarchical animation data
- **HTreeClass (Class)**: Hierarchy tree data
- **Font3DDataClass (Class)**: 3D font data management

## Key Functions
### Load_3D_Assets
- Purpose: Load 3D assets from file
- Calls: Load_Prototype, Find_Prototype_Loader

### Create_Render_Obj
- Purpose: Create an instance of a named render object
- Calls: Find_Prototype, PrototypeClass methods

### Get_Texture
- Purpose: Retrieve or create a texture resource
- Calls: TextureHash operations, TextureFileCache methods

### Register_Prototype_Loader
- Purpose: Add custom prototype loaders
- Calls: PrototypeLoaders vector operations

## Globals
- **TheInstance (WW3DAssetManager*)**: Singleton instance of the asset manager
- **WW3D_Load_On_Demand (bool)**: Controls lazy loading behavior
- **Activate_Fog_On_Load (bool)**: Controls fog activation during loading

## Dependencies
- Key includes: "always.h", "vector.h", "htreemgr.h", "hanimmgr.h", "texture.h"
- External symbols: DynamicVectorClass, HashTemplateClass, StringClass, FileClass
- Forward declarations: HAnimClass, HTreeClass, RenderObjClass, etc.
