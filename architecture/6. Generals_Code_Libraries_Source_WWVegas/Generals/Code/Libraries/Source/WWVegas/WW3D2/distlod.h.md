# Generals/Code/Libraries/Source/WWVegas/WW3D2/distlod.h

## Purpose
Defines classes for distance-based Level of Detail (LOD) rendering in the SAGE engine.

## Responsibilities
- Declares `DistLODClass` for managing multiple resolution models
- Defines LOD definition and loading infrastructure
- Provides prototype system for asset management
- Handles model switching based on camera distance

## Key Types
- **DistLODClass (Class)**: Manages multiple resolution models and switches between them based on distance
- **DistLODDefClass (Class)**: Contains definition data for a distance-based LOD object
- **DistLODNodeDefStruct (Struct)**: Describes a single model in a LOD object with distance thresholds
- **DistLODLoaderClass (Class)**: Handles loading of LOD objects from W3D files
- **DistLODPrototypeClass (Class)**: Prototype system for LOD objects
- **LODNodeClass (Struct)**: Internal structure holding a model and its distance thresholds
- **HIGHEST_LOD (Enum)**: Constant for highest resolution LOD index

## Key Functions
### DistLODClass::Update_Lod
- Purpose: Updates the current LOD based on camera distance
- Calls: Not inferable

### DistLODClass::Increment_Lod
- Purpose: Switches to a lower resolution LOD
- Calls: Not inferable

### DistLODClass::Decrement_Lod
- Purpose: Switches to a higher resolution LOD
- Calls: Not inferable

### DistLODDefClass::Load_W3D
- Purpose: Loads LOD definition from a W3D chunk
- Calls: `read_header`, `read_node`

### DistLODPrototypeClass::Create
- Purpose: Creates a new DistLODClass instance from prototype
- Calls: Not inferable

## Globals
- **_DistLODLoader (DistLODLoaderClass)**: Global instance of the LOD loader for asset manager

## Dependencies
- `proto.h`, `rendobj.h`, `composite.h`, `w3derr.h`
- `ChunkLoadClass`, `RenderObjClass`, `PrototypeClass`, `W3DMPO`, `HAnimClass`, `HAnimComboClass`, `CameraClass`, `RayCollisionTestClass`, `AABoxCollisionTestClass`, `OBBoxCollisionTestClass`
