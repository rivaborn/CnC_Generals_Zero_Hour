# Generals/Code/Libraries/Source/WWVegas/WW3D2/composite.cpp

## Purpose
Implements the `CompositeRenderObjClass`, a render object that manages a collection of sub-objects and delegates operations to them.

## Responsibilities
- Manages a hierarchy of sub-render objects
- Delegates rendering and collision operations to sub-objects
- Handles object naming and bounding volume updates
- Propagates notifications and state changes to sub-objects

## Key Types
- **CompositeRenderObjClass (Class)**: Composite render object that contains and manages other render objects
- **RenderObjClass (Class)**: Base render object class (external)
- **SceneClass (Class)**: Scene management class (external)
- **RayCollisionTestClass, AABoxCollisionTestClass, OBBoxCollisionTestClass (Classes)**: Collision test classes (external)
- **AABoxIntersectionTestClass, OBBoxIntersectionTestClass (Classes)**: Intersection test classes (external)
- **DecalGeneratorClass (Class)**: Decal generation class (external)

## Key Functions
### `Restart`
- Purpose: Recursively restarts all sub-objects
- Calls: `RenderObjClass::Restart`

### `Get_Num_Polys`
- Purpose: Returns the total number of polygons across all sub-objects
- Calls: `RenderObjClass::Get_Num_Polys`

### `Notify_Added`
- Purpose: Notifies all sub-objects that they were added to a scene
- Calls: `RenderObjClass::Notify_Added`

### `Notify_Removed`
- Purpose: Notifies all sub-objects that they were removed from a scene
- Calls: `RenderObjClass::Notify_Removed`

### `Cast_Ray`
- Purpose: Casts a ray against all sub-objects
- Calls: `RenderObjClass::Cast_Ray`

### `Cast_AABox`
- Purpose: Casts an axis-aligned box against all sub-objects
- Calls: `RenderObjClass::Cast_AABox`

### `Cast_OBBox`
- Purpose: Casts an oriented box against all sub-objects
- Calls: `RenderObjClass::Cast_OBBox`

### `Intersect_AABox`
- Purpose: Intersects with an axis-aligned box against all sub-objects
- Calls: `RenderObjClass::Intersect_AABox`

### `Intersect_OBBox`
- Purpose: Intersects with an oriented box against all sub-objects
- Calls: `RenderObjClass::Intersect_OBBox`

### `Create_Decal`
- Purpose: Creates a decal on all sub-objects
- Calls: `RenderObjClass::Create_Decal`

### `Delete_Decal`
- Purpose: Removes decals with a given ID from all sub-objects
- Calls: `RenderObjClass::Delete_Decal`

### `Update_Obj_Space_Bounding_Volumes`
- Purpose: Updates the object-space bounding volumes by combining sub-objects' volumes
- Calls: `RenderObjClass::Get_Obj_Space_Bounding_Sphere`, `RenderObjClass::Get_Obj_Space_Bounding_Box`, `RenderObjClass::Invalidate_Cached_Bounding_Volumes`

### `Set_User_Data`
- Purpose: Sets user data for this object and optionally all sub-objects recursively
- Calls: `RenderObjClass::Set_User_Data`

## Globals
- **None**

## Dependencies
- `composite.h` (header for this class)
- `wwdebug.h` (debug utilities)
- `stdlib.h`, `string.h` (standard C libraries)
- `RenderObjClass`, `SceneClass`, collision test classes
