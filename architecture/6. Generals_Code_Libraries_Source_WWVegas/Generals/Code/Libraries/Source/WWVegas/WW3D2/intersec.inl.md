# Generals/Code/Libraries/Source/WWVegas/WW3D2/intersec.inl

## Purpose
Inline functions for 3D intersection tests and polygon clipping operations in the SAGE engine.

## Responsibilities
- Ray-screen coordinate conversion
- Point-in-polygon tests (2D/3D)
- Triangle intersection and clipping
- Plane intersection calculations

## Key Types
- `IntersectionClass`: Core intersection testing class
- `IntersectionResultClass`: Stores intersection results (range, alpha/beta, intersection point)
- `Vector3`/`Vector2`: Math types (external)

## Key Functions
### `Get_Screen_Ray`
- Purpose: Convert screen coordinates to a world-space ray
- Calls: `camera->Get_Transform()`, `camera->Get_Position()`, `camera->Get_Viewport()`

### `_Point_In_Polygon_Z`
- Purpose: Test if a point lies within a 3D triangle (optimized for Z-axis)
- Calls: None (pure math)

### `Intersect_Polygon_Z`
- Purpose: Test ray intersection with a Z-aligned polygon
- Calls: `Plane_Z_Distance()`, `_Point_In_Polygon()`

### `Clip_Triangle_To_LineXY`
- Purpose: Clip a triangle against a 2D line segment
- Calls: `In_Front_Of_Line()`, `Intersect_Lines()`

### `_Intersect_Triangles_Z`
- Purpose: Compute intersection between two triangles with UV mapping
- Calls: `Clip_Triangle_To_LineXY()`, `_Point_In_Polygon()`

## Globals
- `DEBUG_NORMALS`: Debug flag for normal verification
- `AXIS_1`/`AXIS_2`/`AXIS_3`: Axis defines (0,1,2)

## Dependencies
- `camera.h` (CameraClass, ViewportClass)
- `Vector3`/`Vector2` math types
- Debug printing (DEBUG_NORMALS only)
