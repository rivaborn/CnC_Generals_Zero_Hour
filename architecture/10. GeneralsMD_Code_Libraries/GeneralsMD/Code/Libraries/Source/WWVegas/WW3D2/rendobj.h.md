# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/rendobj.h

## Purpose
Defines the base class `RenderObjClass` for all renderable objects in the WW3D engine, including interfaces for rendering, collision detection, hierarchical animation, and LOD management.

## Responsibilities
- Provides core rendering interface (Render, Special_Render)
- Manages scene graph relationships (Add/Remove, Container hierarchy)
- Handles collision detection (ray, box intersections)
- Supports hierarchical animation and bone control
- Implements predictive LOD system and bounding volumes

## Key Types
- **RenderObjClass (Class)**: Base class for all renderable objects.
- **RenderHookClass (Class)**: Interface for pre/post-render hooks.
- **Material_Override (Struct)**: Custom material settings for meshes.
- **AnimMode (Enum)**: Animation playback modes (loop, once, etc.).
- **CLASSID_* (Enum)**: Class IDs for render object types (mesh, model, etc.).

## Key Functions
### `Render(RenderInfoClass &rinfo)`
- Purpose: Renders the object using the provided render info.
- Calls: None (pure virtual).

### `Cast_Ray(RayCollisionTestClass &raytest)`
- Purpose: Tests ray intersection with the object.
- Calls: None (default returns false).

### `Get_Bounding_Sphere()`
- Purpose: Returns the object's bounding sphere (lazy-updated).
- Calls: `Update_Cached_Bounding_Volumes()` if invalid.

### `Validate_Transform()`
- Purpose: Ensures the transform is up-to-date if the container moved.
- Calls: None (protected).

## Globals
- **AT_MIN_LOD (float)**: Sentinel for minimum LOD value.
- **AT_MAX_LOD (float)**: Sentinel for maximum LOD value.

## Dependencies
- Key includes: `always.h`, `refcount.h`, `sphere.h`, `coltype.h`, `aabox.h`, `persist.h`, `multilist.h`, `robjlist.h`
- External symbols: `Vector3`, `Matrix3D`, `MaterialInfoClass`, `SceneClass`, etc. (forward-declared).
