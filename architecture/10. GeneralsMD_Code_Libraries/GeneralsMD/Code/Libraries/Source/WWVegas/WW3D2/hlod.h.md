# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hlod.h

## Purpose
Defines hierarchical level-of-detail (HLOD) model classes for the W3D engine, including loading, rendering, and animation support.

## Responsibilities
- Defines HLOD model hierarchy and LOD management
- Provides rendering, collision, and animation interfaces
- Handles model loading/saving via W3D chunks
- Manages sub-objects, proxies, and snap points
- Implements predictive LOD selection

## Key Types
- **HLodClass (Class)**: Hierarchical animatable LOD model container
- **HLodDefClass (Class)**: W3D chunk definition for HLOD models
- **HLodLoaderClass (Class)**: Prototype loader for HLOD assets
- **HLodPrototypeClass (Class)**: Prototype factory for HLOD instances
- **ModelNodeClass (Struct)**: Pair of model pointer and bone index
- **ModelArrayClass (Class)**: Dynamic array of ModelNodeClass with LOD metrics
- **SubObjectArrayClass (Class)**: Describes LOD sub-objects with bone attachments

## Key Functions
### HLodClass::Render
- Purpose: Renders the current LOD based on camera distance
- Calls: Not visible in header

### HLodClass::Prepare_LOD
- Purpose: Calculates LOD factors for predictive LOD selection
- Calls: Not visible in header

### HLodDefClass::Load_W3D
- Purpose: Loads HLOD definition from W3D chunk
- Calls: ChunkLoadClass methods

### HLodLoaderClass::Load_W3D
- Purpose: Factory method for creating HLOD from W3D data
- Calls: ChunkLoadClass methods

## Globals
- **_HLodLoader (HLodLoaderClass)**: Singleton loader instance for asset manager

## Dependencies
- animobj.h, vector.h, snappts.h, proto.h, w3derr.h, proxy.h
- W3DMPO (memory management), PrototypeLoaderClass, PrototypeClass
- RenderObjClass, Animatable3DObjClass, HAnimClass, HAnimComboClass
- ChunkLoadClass, ChunkSaveClass, SceneClass, CameraClass
- Collision test classes (RayCollisionTestClass, etc.)
