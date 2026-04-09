# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/composite.cpp

## Purpose
Implements the `CompositeRenderObjClass`, a render object that manages a collection of sub-objects and delegates operations to them.

## Responsibilities
- Manages a hierarchy of sub-render objects
- Delegates rendering and collision operations to sub-objects
- Maintains combined bounding volumes for the composite
- Handles notifications and lifecycle events for sub-objects

## Key Types
- **CompositeRenderObjClass (Class)**: Composite render object that contains and manages other render objects
- **StringClass (Type)**: Used for storing object names (inherited)

## Key Functions
### `Restart`
- Purpose: Recursively restarts all sub-objects
- Calls: `RenderObjClass::Restart`

### `Get_Num_Polys`
- Purpose: Returns total polygon count across all sub-objects
- Calls: `RenderObjClass::Get_Num_Polys`

### `Notify_Added`/`Notify_Removed`
- Purpose: Propagates scene addition/removal notifications to sub-objects
- Calls: `RenderObjClass::Notify_Added`/`Notify_Removed`

### `Cast_Ray`/`Cast_AABox`/`Cast_OBBox`
- Purpose: Performs collision tests by delegating to sub-objects
- Calls: Respective collision test methods on sub-objects

### `Update_Obj_Space_Bounding_Volumes`
- Purpose: Computes combined bounding volumes from all sub-objects
- Calls: `Get_Obj_Space_Bounding_Sphere`, `Get_Obj_Space_Bounding_Box`

### `Set_User_Data`
- Purpose: Sets user data on this object and optionally all sub-objects
- Calls: `RenderObjClass::Set_User_Data`

## Globals
- **Name (const char*)**: Object name
- **BaseModelName (StringClass)**: Base model name (may be empty)

## Dependencies
- `composite.h` (header)
- `wwdebug.h` (assertions)
- `RenderObjClass` (base class)
- `SceneClass` (scene management)
- `RayCollisionTestClass`, `AABoxCollisionTestClass`, etc. (collision testing)
- `DecalGeneratorClass` (decal management)
