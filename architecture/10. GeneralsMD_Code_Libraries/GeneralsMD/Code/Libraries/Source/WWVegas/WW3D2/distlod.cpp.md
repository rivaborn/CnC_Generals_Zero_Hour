# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/distlod.cpp

## Purpose
Handles distance-based Level of Detail (LOD) rendering for 3D models in the SAGE engine.

## Responsibilities
- Loads and manages DistLOD model definitions from W3D files
- Controls LOD switching based on camera distance
- Provides rendering and collision testing for LOD models
- Manages bone transformations across all LOD levels

## Key Types
- **DistLODDefClass**: Blueprint for creating DistLOD models
- **DistLODClass**: Runtime LOD model container
- **DistLODLoaderClass**: W3D file loader for DistLOD models
- **DistLODPrototypeClass**: Prototype creation for DistLOD models
- **LODNodeClass**: Internal structure for storing LOD model references

## Key Functions
### DistLODPrototypeClass::Create
- Purpose: Creates a new DistLOD instance from a prototype
- Calls: NEW_REF, nstrdup, W3DNEWARRAY, HLodClass constructor

### DistLODLoaderClass::Load_W3D
- Purpose: Loads DistLOD model from W3D file
- Calls: DistLODDefClass::Load_W3D, DistLODPrototypeClass constructor

### DistLODClass::Update_Lod
- Purpose: Adjusts current LOD based on camera distance
- Calls: CameraClass::Get_Position, Increment_Lod, Decrement_Lod

### DistLODClass::Increment_Lod/Decrement_Lod
- Purpose: Switches to higher/lower detail LOD
- Calls: Notify_Added, Notify_Removed

## Globals
- **_DistLODLoader** (DistLODLoaderClass): Singleton loader instance

## Dependencies
- distlod.h, nstrdup.h, ww3d.h, assetmgr.h, camera.h
- w3derr.h, wwdebug.h, chunkio.h, hlod.h, rinfo.h
- coltest.h, inttest.h
