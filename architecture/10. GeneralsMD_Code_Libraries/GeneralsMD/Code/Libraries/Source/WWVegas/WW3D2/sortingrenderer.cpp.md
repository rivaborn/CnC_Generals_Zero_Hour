# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/sortingrenderer.cpp

## Purpose
Handles depth-sorted rendering of triangles in the SAGE engine, managing sorting nodes and dynamic buffers.

## Responsibilities
- Manages sorting of triangles by depth for correct transparency rendering
- Handles dynamic vertex/index buffer allocation for sorted geometry
- Implements custom sorting algorithms (hybrid quicksort/insertion sort)
- Maintains lists of sorting nodes and clean-up mechanisms
- Supports volume particle rendering with depth layers

## Key Types
- **ShortVectorIStruct (struct)**: Stores three unsigned short indices for triangle vertices
- **TempIndexStruct (struct)**: Temporary structure for sorting with triangle indices and depth (z) value
- **SortingNodeStruct (class)**: Node containing render state, bounding sphere, and geometry references for sorting
- **None**: No enums defined

## Key Functions
### InsertionSort
- Purpose: Performs insertion sort on TempIndexStruct array
- Calls: None (pure algorithm)

### Sort
- Purpose: Hybrid quicksort/insertion sort implementation for TempIndexStruct
- Calls: InsertionSort, std::swap

### Get_Sorting_Struct
- Purpose: Retrieves or creates a SortingNodeStruct from clean list
- Calls: W3DNEW

### Get_Temp_Index_Array
- Purpose: Allocates or reuses temporary index array for sorting
- Calls: W3DNEWARRAY

### Release_Refs
- Purpose: Releases all references in a SortingNodeStruct
- Calls: REF_PTR_RELEASE

### Apply_Render_State
- Purpose: Applies render state to DX8 wrapper
- Calls: DX8Wrapper::Set_Shader, Set_Material, Set_Texture, Set_DX8_Light

## Globals
- **DEFAULT_SORTING_POLY_COUNT (unsigned)**: Default maximum polygon count (16384)
- **DEFAULT_SORTING_VERTEX_COUNT (unsigned)**: Default maximum vertex count (32768)
- **sorted_list (DLListClass)**: List of nodes to be sorted
- **clean_list (DLListClass)**: List of reusable nodes
- **temp_index_array (TempIndexStruct**)**: Temporary array for sorting indices
- **overlapping_node_count (unsigned)**: Count of nodes in current sorting batch
- **MAX_OVERLAPPING_NODES (unsigned)**: Maximum nodes in a batch (4096)

## Dependencies
- sortingrenderer.h, dx8vertexbuffer.h, dx8indexbuffer.h, dx8wrapper.h
- vertmaterial.h, texture.h, d3d8.h, D3dx8math.h, statistics.h
- wwprofile.h, algorithm
- W3D memory allocation macros (W3DNEW, W3DNEWARRAY)
- DX8Wrapper class methods
- DLListClass, DLNodeClass templates
- Vector3, SphereClass, Matrix4x4 classes
