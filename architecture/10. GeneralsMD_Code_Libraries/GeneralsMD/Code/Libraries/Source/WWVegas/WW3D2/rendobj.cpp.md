# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/rendobj.cpp

## Purpose
Implements the `RenderObjClass` and its persistence system for the SAGE engine's 3D rendering pipeline.

## Responsibilities
- Manages render object creation, transformation, and scene integration
- Handles collision detection and intersection tests
- Implements dependency tracking for assets and textures
- Provides persistence support via `RenderObjPersistFactoryClass`
- Utility functions for filename conversion and transform validation

## Key Types
- **RenderObjClass (Class)**: Base class for all renderable objects in the scene
- **RenderObjPersistFactoryClass (Class)**: Handles saving/loading of render objects
- **(anonymous enum) (Enum)**: Defines chunk IDs for persistence
- **RENDOBJFACTORY_CHUNKID_VARIABLES (Enum)**: Chunk ID constant
- **RENDOBJFACTORY_VARIABLE_OBJPOINTER (Enum)**: Micro-chunk ID for object pointer
- **RENDOBJFACTORY_VARIABLE_NAME (Enum)**: Micro-chunk ID for object name
- **RENDOBJFACTORY_VARIABLE_TRANSFORM (Enum)**: Micro-chunk ID for transform

## Key Functions
### Filename_From_Asset_Name
- Purpose: Converts an asset name to a W3D filename by appending ".w3d"
- Calls: `::lstrcpy`, `::strchr`, `StringClass::Get_Buffer`, `StringClass::operator+=`

### Check_Is_Transform_Identity
- Purpose: Checks if a 3D matrix represents an identity transform
- Calls: None (inline function)

### RenderObjPersistFactoryClass::Load
- Purpose: Loads a render object from a chunk stream
- Calls: `WW3DAssetManager::Get_Instance()->Create_Render_Obj`, `SaveLoadSystemClass::Register_Pointer`

### RenderObjPersistFactoryClass::Save
- Purpose: Saves a render object to a chunk stream
- Calls: `ChunkSaveClass::Begin_Chunk`, `WRITE_MICRO_CHUNK`, `ChunkSaveClass::End_Chunk`

## Globals
- **_RenderObjPersistFactory (RenderObjPersistFactoryClass)**: Static instance of the persistence factory

## Dependencies
- Key includes: `rendobj.h`, `assetmgr.h`, `scene.h`, `chunkio.h`, `persistfactory.h`
- External symbols: `WW3DAssetManager`, `SaveLoadSystemClass`, `WWDEBUG_SAY`, `WWASSERT`
