# Generals/Code/Libraries/Source/WWVegas/WW3D2/meshbuild.cpp

## Purpose
Implements mesh processing functionality for the SAGE engine, including vertex/face optimization, normal computation, and triangle strip generation.

## Responsibilities
- Mesh optimization (vertex/face deduplication, triangle strips)
- Normal computation (face and vertex)
- Bounding volume calculation
- Degenerate face removal
- Vertex/face sorting and hashing

## Key Types
- **FaceHasherClass (Class)**: Hash calculator for detecting duplicate faces
- **VertexArrayClass (Class)**: Manages unique vertices with smoothing group handling
- **COMPARE_FUNC_TYPE (typedef)**: Function pointer for qsort comparisons
- **HASH_TABLE_SIZE (enum)**: Size constant for vertex hashing

## Key Functions
### `Submit_Vertex`
- Purpose: Adds a vertex to the vertex array, handling duplicates and smoothing groups
- Calls: `Verts_Match`, `Verts_Shading_Match`, `compute_hash`

### `Strip_Optimize_Mesh`
- Purpose: Optimizes mesh into triangle strips for rendering efficiency
- Calls: Memory allocation/deallocation, edge/polygon processing functions

### `Sort_Vertices`
- Purpose: Sorts vertices by bone index and material for better cache locality
- Calls: `qsort`, `vertex_compare`

## Globals
- **EPSILON (float)**: Precision threshold for floating-point comparisons
- **Texture_Compare_Funcs (array)**: Array of comparison functions for texture sorting

## Dependencies
- `meshbuild.h`, `uarray.h`, `stdlib.h`, `string.h`, `assert.h`
- `Vector3`, `HashCalculatorClass`, `W3DNEWARRAY` (memory allocation)
