# Generals/Code/Tools/WW3D/max2w3d/meshbuild.cpp

## Purpose
Handles mesh processing and optimization for the WW3D engine, including vertex/face management and triangle strip generation.

## Responsibilities
- Manages vertex and face data structures
- Optimizes meshes for rendering (triangle strips)
- Handles vertex/face uniqueness and hashing
- Computes mesh statistics and bounds
- Implements sorting and comparison functions for mesh elements

## Key Types
- **FaceHasherClass (Class)**: Hash calculator for detecting duplicate faces
- **VertexArrayClass (Class)**: Manages unique vertices with smoothing group handling
- **COMPARE_FUNC_TYPE (Class)**: Function pointer type for qsort comparisons
- **(anonymous enum) (Enum)**: Defines HASH_TABLE_SIZE constant
- **HASH_TABLE_SIZE (Enum)**: Size constant for vertex hash table

## Key Functions
### `Submit_Vertex`
- Purpose: Adds a vertex to the vertex array, checking for duplicates
- Calls: `Verts_Match`, `Verts_Shading_Match`, `compute_hash`

### `Strip_Optimize_Mesh`
- Purpose: Optimizes mesh into triangle strips
- Calls: Memory allocation/deallocation, array operations

### `Sort_Vertices`
- Purpose: Sorts vertices by bone index and material
- Calls: `qsort`, `vertex_compare`

### `tex_compare`
- Purpose: Compares faces by texture and vertex material
- Calls: None (inline function)

## Globals
- **EPSILON (float)**: Small value for floating-point comparisons
- **Texture_Compare_Funcs (COMPARE_FUNC_TYPE[4][2])**: Array of comparison functions for different passes/stages

## Dependencies
- `meshbuild.h`, `uarray.h`, `stdlib.h`, `string.h`, `assert.h`
- Uses `Vector3`, `HashCalculatorClass` templates
- Depends on `MeshBuilderClass` definitions (VertClass, FaceClass)
