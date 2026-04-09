# Generals/Code/Libraries/Source/WWVegas/WW3D2/collect.cpp

## Purpose
Manages collection objects in the W3D engine, including definitions, prototypes, and runtime instances.

## Responsibilities
- Defines `CollectionDefClass` for blueprint data
- Implements `CollectionPrototypeClass` for object creation
- Handles `CollectionClass` for runtime rendering and collision
- Loads collection data from W3D files
- Manages sub-object hierarchies and bounding volumes

## Key Types
- **CollectionDefClass (Class)**: Blueprint for collection objects
- **CollectionPrototypeClass (Class)**: Prototype for creating collection instances
- **CollectionClass (Class)**: Runtime collection object with rendering/collision

## Key Functions
### CollectionClass::Render
- Purpose: Renders all sub-objects in the collection
- Calls: `SubObjects[i]->Render()`

### CollectionClass::Update_Obj_Space_Bounding_Volumes
- Purpose: Recomputes bounding sphere/box from sub-objects
- Calls: `SubObjects[i]->Get_Bounding_Sphere()`, `SubObjects[i]->Get_Bounding_Box()`

### CollectionDefClass::Load
- Purpose: Loads collection definition from W3D file
- Calls: `cload.Read()`, `SnapPoints->Load_W3D()`

### CollectionLoaderClass::Load_W3D
- Purpose: Factory method for loading collections
- Calls: `def->Load()`, `NEW CollectionPrototypeClass()`

## Globals
- **_CollectionLoader (CollectionLoaderClass)**: Singleton for loading collections

## Dependencies
- `collect.h`, `chunkio.h`, `camera.h`, `wwdebug.h`, `snappts.h`, `assetmgr.h`, `ww3d.h`, `w3derr.h`
- `DynamicVectorClass`, `Matrix3D`, `Vector3`, `W3DMPO`, `PrototypeClass`, `RenderObjClass`
