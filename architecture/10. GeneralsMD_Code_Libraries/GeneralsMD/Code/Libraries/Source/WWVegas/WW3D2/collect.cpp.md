# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/collect.cpp

## Purpose
Manages collection objects in the W3D engine, including definitions, prototypes, and runtime instances.

## Responsibilities
- Defines `CollectionDefClass` (blueprint) and `CollectionPrototypeClass` (prototype)
- Implements `CollectionClass` for runtime collection rendering
- Handles loading W3D collection assets and managing sub-objects
- Provides collision, rendering, and transformation logic for collections

## Key Types
- **CollectionDefClass (Class)**: Blueprint for collection objects, stores names and snap points
- **CollectionPrototypeClass (Class)**: Prototype for creating collection instances
- **CollectionClass (Class)**: Runtime collection object with rendering and collision logic

## Key Functions
### CollectionClass::Render
- Purpose: Renders all sub-objects in the collection
- Calls: `SubObjects[i]->Render(rinfo)`, `Update_Sub_Object_Transforms()`

### CollectionClass::Update_Obj_Space_Bounding_Volumes
- Purpose: Recomputes object-space bounding volumes for the collection
- Calls: `SubObjects[i]->Get_Bounding_Sphere()`, `SubObjects[i]->Get_Bounding_Box()`

### CollectionDefClass::Load
- Purpose: Loads collection definition from a W3D file
- Calls: `cload.Open_Chunk()`, `cload.Read()`, `SnapPoints->Load_W3D()`

### CollectionLoaderClass::Load_W3D
- Purpose: Factory method to create a collection prototype from a W3D file
- Calls: `def->Load(cload)`, `NEW CollectionPrototypeClass(def)`

## Globals
- **_CollectionLoader (CollectionLoaderClass)**: Global loader instance for W3D collections

## Dependencies
- Key includes: `collect.h`, `chunkio.h`, `camera.h`, `wwdebug.h`, `snappts.h`, `assetmgr.h`, `ww3d.h`, `w3derr.h`
- External symbols: `WW3DAssetManager`, `W3DMPO`, `PrototypeClass`, `RenderObjClass`, `CompositeRenderObjClass`
