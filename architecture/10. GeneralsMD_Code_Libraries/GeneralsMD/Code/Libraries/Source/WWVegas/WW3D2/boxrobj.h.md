# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/boxrobj.h

## Purpose
Defines render objects for axis-aligned and oriented bounding boxes used in collision detection.

## Responsibilities
- Provides base class for box render objects
- Implements AABox and OBBox render objects with collision testing
- Manages box prototype loading and instantiation
- Handles box rendering with display mask control

## Key Types
- **VertexMaterialClass (Class)**: Not inferable.
- **BoxRenderObjClass (Class)**: Base class for box render objects.
- **AABoxRenderObjClass (Class)**: Axis-aligned box render object.
- **OBBoxRenderObjClass (Class)**: Oriented bounding box render object.
- **BoxLoaderClass (Class)**: Loader for box prototypes.
- **BoxPrototypeClass (Class)**: Prototype for box objects.

## Key Functions
### BoxRenderObjClass::Set_Local_Center_Extent
- Purpose: Sets the local center and extent of the box.
- Calls: update_cached_box()

### BoxRenderObjClass::Set_Local_Min_Max
- Purpose: Sets the local min and max bounds of the box.
- Calls: update_cached_box()

### AABoxRenderObjClass::Get_Box
- Purpose: Returns the cached AABox.
- Calls: Validate_Transform(), update_cached_box()

### OBBoxRenderObjClass::Get_Box
- Purpose: Returns the cached OBBox.
- Calls: None

## Globals
- **_BoxLoader (BoxLoaderClass)**: Instance of the box loader for asset management.

## Dependencies
- Key includes: "always.h", "rendobj.h", "w3d_file.h", "shader.h", "proto.h", "obbox.h"
- External symbols: W3DMPO, RenderObjClass, PrototypeClass, W3dBoxStruct, AABoxClass, OBBoxClass, Vector3, Matrix3D, RayCollisionTestClass, AABoxCollisionTestClass, OBBoxCollisionTestClass, AABoxIntersectionTestClass, OBBoxIntersectionTestClass, SphereClass, ChunkLoadClass, W3D_CHUNK_BOX
