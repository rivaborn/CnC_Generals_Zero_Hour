# Generals/Code/Libraries/Source/WWVegas/WW3D2/intersec.cpp

## Purpose
Handles ray-object intersection tests for the 3D rendering system.

## Responsibilities
- Performs ray-box and ray-sphere intersection tests
- Manages hierarchical object intersection queries
- Provides screen-point to world-ray conversion
- Supports layer-based intersection testing

## Key Types
- **IntersectionClass**: Main intersection testing class
- **IntersectionResultClass**: Stores intersection results (point, normal, range)
- **Vector3**: 3D vector type

## Key Functions
### Intersect_Screen_Point_RenderObject
- Purpose: Tests intersection between screen point and render object
- Calls: Get_Screen_Ray, Intersect_RenderObject

### Intersect_Layer
- Purpose: Tests intersection with all objects in a layer
- Calls: SceneIterator methods, RenderObjClass::Intersect

### Intersect_Box
- Purpose: Tests ray-box intersection using fast algorithm
- Calls: None (standalone implementation)

### Intersect_Hierarchy
- Purpose: Tests intersection with hierarchical object structures
- Calls: Append_Hierarchy_Objects, Intersect_Object_Array

## Globals
- **_RayLocation** (Vector3): Current ray origin
- **_RayDirection** (Vector3): Current ray direction
- **_IntersectionNormal** (Vector3): Last intersection normal

## Dependencies
- "intersec.h", "camera.h", "scene.h", "intersec.inl"
- LayerClass, ViewportClass, SceneIterator, RenderObjClass
