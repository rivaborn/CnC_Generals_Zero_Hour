# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hlod.cpp

## Purpose
Implements the HLOD (Hierarchical Level of Detail) system for the W3D engine, handling loading, rendering, and management of hierarchical models with multiple LOD levels.

## Responsibilities
- Loads and saves HLOD definitions from/to W3D files
- Manages hierarchical model structures with multiple LOD levels
- Handles proxy objects and bone associations
- Provides rendering and transformation capabilities for HLODs
- Supports model scaling, decal management, and bounding volume updates

## Key Types
- **ProxyRecordClass (Class)**: Stores bone index and name for proxy objects
- **ProxyArrayClass (Class)**: Ref-counted list of proxy objects
- **HLodLoaderClass (Class)**: Handles loading of HLOD definitions from W3D files
- **HLodPrototypeClass (Class)**: Creates HLOD instances from definitions
- **HLodDefClass (Class)**: Stores HLOD definition data (name, hierarchy, LODs, proxies)
- **HLodClass (Class)**: Main HLOD implementation with rendering and management functions

## Key Functions
### HLodLoaderClass::Load_W3D
- Purpose: Loads an HLOD definition from a W3D file
- Calls: HLodDefClass::Load_W3D, HLodPrototypeClass constructor

### HLodClass::Scale
- Purpose: Scales the HLOD and all its sub-objects by a factor
- Calls: RenderObjClass::Scale, HTreeClass::Scale, Update_Obj_Space_Bounding_Volumes

### HLodClass::Update_Sub_Object_Transforms
- Purpose: Updates transforms for all sub-objects based on hierarchy tree
- Calls: Animatable3DObjClass::Update_Sub_Object_Transforms, HTreeClass::Get_Transform

### HLodClass::Update_Obj_Space_Bounding_Volumes
- Purpose: Updates object-space bounding volumes for the HLOD
- Calls: HTreeClass::Base_Update, RenderObjClass::Get_Obj_Space_Bounding_Sphere/Box

## Globals
- **_HLodLoader (HLodLoaderClass)**: Global instance of the HLOD loader

## Dependencies
- Key includes: "hlod.h", "assetmgr.h", "hmdldef.h", "w3derr.h", "chunkio.h", "predlod.h", "rinfo.h", "sphere.h", "boxrobj.h"
- External symbols: W3DNEW, W3DNEWARRAY, WWASSERT, WWDEBUG_SAY, REF_PTR_RELEASE, Matrix3D, Vector3, SphereClass, AABoxClass, MinMaxAABoxClass
