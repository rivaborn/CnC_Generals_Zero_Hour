# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/intersec.inl

## Purpose
Inline functions for 3D intersection tests and ray-polygon interactions in the SAGE engine.

## Responsibilities
- Ray-screen coordinate conversion
- Point-in-polygon tests (2D/3D)
- Triangle clipping and intersection
- Plane intersection calculations

## Key Types
- `IntersectionClass`: Core intersection utilities
- `IntersectionResultClass`: Stores intersection results (range, alpha/beta, intersection point)
- `Vector2/Vector3`: Math types for points/vectors

## Key Functions
### `Get_Screen_Ray`
- Purpose: Convert screen coordinates to a world-space ray
- Calls: `camera->Get_Transform()`, `camera->Get_Position()`, `camera->Get_Viewport()`

### `_Point_In_Polygon_Z`
- Purpose: Test if a point lies inside a 3D triangle (optimized for Z-axis)
- Calls: None (pure math)

### `Intersect_Plane_Quick`
- Purpose: Quick plane intersection test (normalized ray)
- Calls: None

### `Clip_Triangle_To_LineXY`
- Purpose: Clip a triangle against a 2D line
- Calls: `In_Front_Of_Line`, `Intersect_Lines`

## Globals
- `AXIS_1/AXIS_2/AXIS_3` (macros): Define dominant plane axes

## Dependencies
- `camera.h` (CameraClass, ViewportClass)
- `Vector2/Vector3` math types
- Debug utilities (DEBUG_NORMALS)
