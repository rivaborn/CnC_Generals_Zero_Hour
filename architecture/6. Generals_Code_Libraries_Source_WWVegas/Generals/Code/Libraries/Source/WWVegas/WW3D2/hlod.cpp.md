# Generals/Code/Libraries/Source/WWVegas/WW3D2/hlod.cpp

## Purpose
Implements hierarchical level-of-detail (HLOD) rendering system for 3D models in the SAGE engine.

## Responsibilities
- Manages HLOD definitions, prototypes, and runtime instances
- Handles LOD transitions, model scaling, and sub-object management
- Implements proxy object system for bone-name associations
- Provides rendering, collision detection, and bounding volume updates

## Key Types
- **ProxyRecordClass (Class)**: Stores bone index and name for proxy objects
- **ProxyArrayClass (Class)**: Ref-counted list of proxy records
- **HLodLoaderClass (Class)**: Singleton loader for W3D HLOD files
- **HLodPrototypeClass (Class)**: Prototype for creating HLOD instances
- **HLodDefClass (Class)**: Definition data for HLODs (serializable)
- **HLodClass (Class)**: Runtime HLOD instance with rendering capabilities

## Key Functions
### HLodLoaderClass::Load_W3D
- Purpose: Loads HLOD definition from W3D file
- Calls: HLodDefClass::Load_W3D, W3DNEW, W3DNEWARRAY

### HLodClass::Scale
- Purpose: Scales entire HLOD and all sub-objects
- Calls: RenderObjClass::Scale, HTreeClass::Scale, Update_Obj_Space_Bounding_Volumes

### HLodClass::Update_Sub_Object_Transforms
- Purpose: Updates transforms for all sub-objects based on hierarchy
- Calls: Animatable3DObjClass::Update_Sub_Object_Transforms, HTreeClass::Get_Transform

### HLodClass::Update_Obj_Space_Bounding_Volumes
- Purpose: Recalculates object-space bounding volumes
- Calls: HTreeClass::Base_Update, RenderObjClass::Get_Obj_Space_Bounding_Sphere/Box

## Globals
- **_HLodLoader (HLodLoaderClass)**: Singleton instance for loading HLODs

## Dependencies
- hlod.h, assetmgr.h, hmdldef.h, w3derr.h, chunkio.h, predlod.h, rinfo.h
- string.h, win.h, sphere.h, boxrobj.h
- W3DMPO, VectorClass, RefCountClass, Matrix3D, SphereClass, AABoxClass
