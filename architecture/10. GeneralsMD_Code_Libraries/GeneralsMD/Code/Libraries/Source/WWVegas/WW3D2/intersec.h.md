# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/intersec.h

## Purpose
Header file defining the `IntersectionClass` for 3D ray intersection tests in the SAGE engine.

## Responsibilities
- Declares intersection test utilities (ray-sphere, ray-plane, ray-polygon)
- Manages intersection result storage and normal interpolation
- Provides screen-space to world-space ray conversion
- Supports hierarchical object intersection traversal

## Key Types
- **IntersectionResultClass (Class)**: Stores results of intersection tests (location, normal, range, etc.)
- **INTERSECTION_TYPE (Enum)**: Defines intersection result types (NONE, GENERIC, POLYGON)
- **IntersectionClass (Class)**: Main intersection testing class with ray configuration and test methods
- **RenderObjClass (Class)**: Forward declaration for renderable objects (external)
- **POLYGONINDEX (typedef)**: Polygon index type (unsigned short)

## Key Functions
### Intersect_Sphere
- Purpose: Tests ray-sphere intersection and calculates intersection point/normal.
- Calls: `Intersect_Sphere_Quick`, `Vector3::Dot_Product`

### Intersect_Polygon
- Purpose: Tests ray-polygon intersection (multiple overloads).
- Calls: Not visible in header (inline in .inl)

### Intersect_Screen_Point_Layer
- Purpose: Converts screen coordinates to world ray and tests against a layer.
- Calls: `Get_Screen_Ray`, layer intersection methods

### Intersect_Object_Array
- Purpose: Tests ray against array of render objects.
- Calls: `Append_Hierarchy_Objects`, object-specific intersection methods

## Globals
- **_RayLocation (Vector3)**: Static storage for temporary intersection objects
- **_RayDirection (Vector3)**: Static storage for temporary intersection objects
- **_IntersectionNormal (Vector3)**: Static storage for temporary intersection objects

## Dependencies
- Key includes: `matrix3d.h`, `layer.h`, `sphere.h`, `coltype.h`
- External symbols: `RenderObjClass`, `LayerClass`, `Vector3`, `Vector2`, `Matrix3D`
