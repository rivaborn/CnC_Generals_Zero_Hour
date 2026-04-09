# Generals/Code/Libraries/Source/WWVegas/WW3D2/hlod.h

## Purpose
Defines hierarchical level-of-detail (HLod) model classes for the SAGE engine, including loading, rendering, and animation support.

## Responsibilities
- Defines HLodClass for hierarchical animatable LOD models
- Provides loading infrastructure via HLodLoaderClass
- Manages LOD definitions and prototypes
- Handles sub-object hierarchy and proxy systems

## Key Types
- **HLodClass (Class)**: Hierarchical animatable LOD model container
- **HLodDefClass (Class)**: Definition object for HLod model contents
- **HLodLoaderClass (Class)**: Prototype loader for HLod objects
- **HLodPrototypeClass (Class)**: Prototype for HLod object instantiation
- **ModelNodeClass (Struct)**: Pair of RenderObjClass* and bone index
- **ModelArrayClass (Class)**: Dynamic vector of ModelNodeClass with LOD metrics
- **SubObjectArrayClass (Class)**: Describes LOD levels in HLod objects

## Key Functions
### HLodClass::Render
- Purpose: Renders the current LOD model
- Calls: Not inferable (implementation in .cpp)

### HLodClass::Prepare_LOD
- Purpose: Prepares LOD selection based on camera
- Calls: Not inferable

### HLodDefClass::Load_W3D
- Purpose: Loads HLod definition from W3D chunk
- Calls: ChunkLoadClass methods, read_header, read_proxy_array

### HLodLoaderClass::Load_W3D
- Purpose: Loads HLod prototype from W3D file
- Calls: ChunkLoadClass methods

## Globals
- **_HLodLoader (HLodLoaderClass)**: Global loader instance for asset manager

## Dependencies
- animobj.h, vector.h, snappts.h, proto.h, w3derr.h, proxy.h
- W3DMPO (memory pool object), Animatable3DObjClass, PrototypeLoaderClass
- ChunkLoadClass, ChunkSaveClass, RenderInfoClass, SpecialRenderInfoClass
- Matrix3D, Vector3, SphereClass, AABoxClass, RayCollisionTestClass, etc.
