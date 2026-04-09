# Generals/Code/Libraries/Source/WWVegas/WW3D2/rendobj.cpp

## Purpose
Implements the `RenderObjClass` base class for 3D renderable objects in the SAGE engine, handling transformations, collision detection, and persistence.

## Responsibilities
- Manages object transformations and spatial properties
- Handles collision detection and intersection tests
- Provides dependency tracking for assets
- Implements persistence via `PersistFactoryClass`
- Maintains object hierarchy and container relationships

## Key Types
- **RenderObjClass (Class)**: Base class for all renderable 3D objects
- **RenderObjPersistFactoryClass (Class)**: Handles save/load of render objects
- **(anonymous enum)**: Chunk IDs for persistence (lines 1177-1183)
- **RENDOBJFACTORY_CHUNKID_VARIABLES (Enum)**: Persistence chunk ID
- **RENDOBJFACTORY_VARIABLE_OBJPOINTER (Enum)**: Persistence variable ID
- **RENDOBJFACTORY_VARIABLE_NAME (Enum)**: Persistence variable ID
- **RENDOBJFACTORY_VARIABLE_TRANSFORM (Enum)**: Persistence variable ID

## Key Functions
### Filename_From_Asset_Name
- Purpose: Converts asset name to filename with .w3d extension
- Calls: `lstrcpy`, `strchr`

### Check_Is_Transform_Identity
- Purpose: Checks if a matrix is an identity transform
- Calls: None (inline)

### RenderObjPersistFactoryClass::Load
- Purpose: Loads render object from chunk data
- Calls: `WW3DAssetManager::Get_Instance()->Create_Render_Obj`, `SaveLoadSystemClass::Register_Pointer`

### RenderObjPersistFactoryClass::Save
- Purpose: Saves render object to chunk data
- Calls: None (uses chunk save macros)

## Globals
- **_RenderObjPersistFactory (RenderObjPersistFactoryClass)**: Static persistence factory instance

## Dependencies
- Key includes: `rendobj.h`, `assetmgr.h`, `scene.h`, `chunkio.h`, `persistfactory.h`
- External symbols: `WW3DAssetManager`, `SaveLoadSystemClass`, `WWDEBUG_SAY`, `WWASSERT`
