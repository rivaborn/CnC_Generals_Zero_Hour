# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/intersec.cpp

## Purpose
Handles ray-object intersection tests for the SAGE engine's 3D rendering system.

## Responsibilities
- Implements ray-box and ray-sphere intersection tests
- Manages hierarchical object intersection queries
- Provides screen-point to world-ray conversion
- Supports layer-based intersection testing
- Handles collision type filtering

## Key Types
- **IntersectionClass**: Core intersection testing class
- **IntersectionResultClass**: Stores intersection results (point, normal, range)
- **Vector3**: 3D vector math structure

## Key Functions
### Intersect_Screen_Point_RenderObject
- Purpose: Tests intersection between screen point and render object
- Calls: Get_Screen_Ray, Intersect_RenderObject

### Intersect_Layer
- Purpose: Tests intersection with all objects in a scene layer
- Calls: SceneIterator methods, RenderObjClass::Intersect

### Intersect_Box
- Purpose: Implements fast ray-box intersection test
- Calls: None (pure math implementation)

### Intersect_Hierarchy
- Purpose: Tests intersection with hierarchical object structures
- Calls: Append_Hierarchy_Objects, Intersect_Object_Array

### Intersect_Object_Array
- Purpose: Finds nearest intersection among object array
- Calls: RenderObjClass::Intersect, Copy_Results

## Globals
- **_RayLocation** (Vector3): Current ray origin
- **_RayDirection** (Vector3): Current ray direction
- **_IntersectionNormal** (Vector3): Last intersection normal
- **Result** (IntersectionResultClass): Default result storage

## Dependencies
- **intersec.h**: Header with class declarations
- **camera.h**: Camera/viewport functionality
- **scene.h**: Scene management and iteration
- **intersec.inl**: Inline implementations
- **RenderObjClass**: Base render object interface
- **LayerClass**: Scene layer management
- **Vector3**: 3D math operations
