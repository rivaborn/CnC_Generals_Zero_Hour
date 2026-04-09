# Generals/Code/Libraries/Source/WWVegas/WW3D2/rendobj.h

## Purpose
Defines the base class `RenderObjClass` for all renderable objects in the WW3D engine, including scene graph management, rendering, collision detection, and LOD handling.

## Responsibilities
- Provides core interface for renderable objects (cloning, rendering, hierarchy)
- Manages scene graph relationships (add/remove from scenes, containers)
- Handles hierarchical animation and bone control
- Implements collision detection (ray/box intersections)
- Supports predictive LOD (Level of Detail) optimization

## Key Types
- **RenderObjClass (Class)**: Base class for all renderable objects in WW3D
- **Material_Override (Struct)**: Custom rendering parameters for mesh materials
- **AnimMode (Enum)**: Animation playback modes (loop, once, ping-pong, etc.)
- **CLASSID_* (Enum)**: Class IDs for different render object types (mesh, model, light, etc.)
- **SphereClass (Class)**: Bounding sphere for collision/visibility
- **AABoxClass (Class)**: Axis-aligned bounding box for collision

## Key Functions
### `Render(RenderInfoClass &)`
- Purpose: Renders the object using the provided render info
- Calls: None (pure virtual)

### `Intersect(IntersectionClass *, IntersectionResultClass *)`
- Purpose: Tests ray intersection with the render object
- Calls: `Intersect_Sphere_Quick`

### `Get_Bounding_Sphere()`
- Purpose: Returns the cached bounding sphere (lazy-updated)
- Calls: `Update_Cached_Bounding_Volumes` if invalid

### `Validate_Transform()`
- Purpose: Ensures transform is up-to-date if container moved/animated
- Calls: None (protected)

### `Bound_Degrees(float)`
- Purpose: Clamps angle between 0-360 degrees
- Calls: None

## Globals
- **AT_MIN_LOD (float)**: Sentinel value for LOD queries
- **AT_MAX_LOD (float)**: Sentinel value for LOD queries
- **TheAnimModeNames (char*)**: String names for animation modes (conditional)

## Dependencies
- `Vector3`, `Matrix3D`, `SphereClass`, `AABoxClass`: Core math types
- `SceneClass`, `HAnimClass`: Scene graph and animation
- `RefCountClass`, `PersistClass`: Memory and serialization
- `DynamicVectorClass`: Dependency list management
- `coltype.h`: Collision type definitions
