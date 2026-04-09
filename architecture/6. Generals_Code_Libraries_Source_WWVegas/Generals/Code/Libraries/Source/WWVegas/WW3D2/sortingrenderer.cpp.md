# Generals/Code/Libraries/Source/WWVegas/WW3D2/sortingrenderer.cpp

## Purpose
Handles 3D rendering sorting for the SAGE engine, managing depth-based triangle sorting for proper transparency and overlap rendering.

## Responsibilities
- Implements sorting algorithms (quick/insertion sort) for rendering order
- Manages sorting nodes with render states and bounding volumes
- Handles dynamic vertex/index buffer allocation for sorted rendering
- Processes overlapping geometry for correct depth rendering
- Provides flush mechanisms to render sorted geometry batches

## Key Types
- **ShortVectorIStruct (struct)**: Stores three unsigned short indices (i,j,k) for triangle vertices
- **TempIndexStruct (struct)**: Associates a ShortVectorIStruct with a node index for sorting
- **SortingNodeStruct (class)**: Contains render state, bounding sphere, and geometry references for sorted rendering
- **None**: No enums defined

## Key Functions
### InsertionSort
- Purpose: Performs insertion sort on array elements using provided keys
- Calls: None (template function)

### QuickSort
- Purpose: Performs quicksort on array elements using provided keys
- Calls: InsertionSort (for small subarrays)

### Sort
- Purpose: Hybrid sorting algorithm that chooses between insertion and quick sort based on data characteristics
- Calls: InsertionSort, QuickSort

### Insert_Triangles
- Purpose: Inserts triangles into the sorting system with bounding sphere and render state
- Calls: Get_Sorting_Struct, DX8Wrapper methods, WWASSERT

### Flush_Sorting_Pool
- Purpose: Renders all sorted geometry in correct depth order
- Calls: Get_Node_Id_Array, Get_Polygon_Z_Array, Get_Polygon_Index_Array, Sort, Apply_Render_State, DX8Wrapper methods

### Flush
- Purpose: Processes all sorted geometry and cleans up resources
- Calls: Insert_To_Sorting_Pool, Flush_Sorting_Pool, DX8Wrapper methods, Release_Refs

## Globals
- **DEFAULT_SORTING_POLY_COUNT (unsigned)**: Default maximum polygon count (16384)
- **DEFAULT_SORTING_VERTEX_COUNT (unsigned)**: Default maximum vertex count (32768)
- **sorted_list (DLListClass)**: List of nodes awaiting sorting
- **clean_list (DLListClass)**: Pool of reusable sorting nodes
- **vertex_z_array (float*)**: Temporary array for vertex Z-depth values
- **polygon_z_array (float*)**: Temporary array for polygon Z-depth values
- **overlapping_node_count (unsigned)**: Count of nodes with depth overlaps
- **MAX_OVERLAPPING_NODES (unsigned)**: Maximum allowed overlapping nodes (1024)

## Dependencies
- sortingrenderer.h, dx8vertexbuffer.h, dx8indexbuffer.h, dx8wrapper.h, vertmaterial.h, texture.h, d3d8.h, D3dx8math.h, statistics.h
- DLNodeClass, DLListClass, W3DMPO_GLUE, Vector3, Matrix4, SphereClass, RenderStateStruct
- DX8Wrapper, DynamicVBAccessClass, DynamicIBAccessClass, SortingVertexBufferClass, SortingIndexBufferClass
