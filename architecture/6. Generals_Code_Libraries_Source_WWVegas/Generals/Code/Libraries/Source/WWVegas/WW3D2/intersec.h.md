# Generals/Code/Libraries/Source/WWVegas/WW3D2/intersec.h

## Purpose
Header file defining the `IntersectionClass` for 3D ray intersection tests in the SAGE engine.

## Responsibilities
- Declares intersection test utilities for 3D geometry
- Defines ray-sphere, ray-plane, and ray-polygon intersection methods
- Provides screen-space to world-space ray conversion
- Supports hierarchy traversal for complex object intersection

## Key Types
- **IntersectionResultClass (Class)**: Stores results of intersection tests (object, polygon, location, normal, etc.)
- **INTERSECTION_TYPE (Enum)**: Type of intersection (NONE, GENERIC, POLYGON)
- **IntersectionClass (Class)**: Main intersection test class with ray configuration and test methods

## Key Functions
### `Set`
- Purpose: Configures ray origin, direction, and test parameters
- Calls: None

### `Intersect_Sphere_Quick`
- Purpose: Fast sphere intersection test (range only)
- Calls: `Vector3::Dot_Product`

### `Intersect_Sphere`
- Purpose: Full sphere intersection with normal calculation
- Calls: `Intersect_Sphere_Quick`, `sqrtf`

### `Get_Screen_Ray`
- Purpose: Converts screen coordinates to world-space ray
- Calls: None (inline declaration)

### `Intersect_Object_Array`
- Purpose: Tests intersection against array of render objects
- Calls: `Append_Hierarchy_Objects`, `Intersect_RenderObject`

### `Intersect_Screen_Point_Layer`
- Purpose: Finds intersection with layer at screen coordinates
- Calls: None (inline declaration)

## Globals
- **_RayLocation (Vector3)**: Static default ray origin
- **_RayDirection (Vector3)**: Static default ray direction
- **_IntersectionNormal (Vector3)**: Static default normal storage

## Dependencies
- `matrix3d.h`, `layer.h`, `sphere.h`, `coltype.h`
- `Vector3`, `Vector2`, `RenderObjClass`, `LayerClass`, `SphereClass`
