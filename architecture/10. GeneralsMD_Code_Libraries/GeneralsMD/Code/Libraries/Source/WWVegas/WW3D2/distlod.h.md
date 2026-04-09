# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/distlod.h

## Purpose
Defines classes for distance-based Level of Detail (LOD) rendering in the W3D engine.

## Responsibilities
- Manages LOD switching based on camera distance
- Handles rendering, animation, and collision for LOD objects
- Provides loading infrastructure for LOD definitions
- Maintains multiple resolution models for a single object

## Key Types
- **DistLODClass (Class)**: Main LOD object that switches between models based on distance
- **DistLODDefClass (Class)**: Definition of an LOD object containing model references and distance thresholds
- **DistLODNodeDefStruct (Struct)**: Describes a single model in an LOD object with distance parameters
- **DistLODLoaderClass (Class)**: Loader for LOD objects from W3D files
- **DistLODPrototypeClass (Class)**: Prototype for creating LOD instances
- **LODNodeClass (Struct)**: Internal structure holding a model and its distance thresholds

## Key Functions
### DistLODClass::Update_Lod
- Purpose: Updates the current LOD based on camera distance
- Calls: Not inferable (implementation in .cpp)

### DistLODClass::Increment_Lod
- Purpose: Switches to a lower resolution LOD
- Calls: Not inferable

### DistLODClass::Decrement_Lod
- Purpose: Switches to a higher resolution LOD
- Calls: Not inferable

### DistLODDefClass::Load_W3D
- Purpose: Loads LOD definition from a W3D chunk
- Calls: read_header, read_node

## Globals
- **_DistLODLoader (DistLODLoaderClass)**: Global loader instance for LOD objects

## Dependencies
- "proto.h", "rendobj.h", "composite.h", "w3derr.h"
- ChunkLoadClass, PrototypeLoaderClass, PrototypeClass, RenderObjClass, CompositeRenderObjClass, W3DMPO
- Matrix3D, Vector3, HAnimClass, HAnimComboClass, RayCollisionTestClass, AABoxCollisionTestClass, OBBoxCollisionTestClass, RenderInfoClass, SpecialRenderInfoClass, CameraClass
