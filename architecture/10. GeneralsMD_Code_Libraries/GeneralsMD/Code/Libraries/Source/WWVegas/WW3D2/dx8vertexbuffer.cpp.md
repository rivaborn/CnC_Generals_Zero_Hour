# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dx8vertexbuffer.cpp

## Purpose
Manages DirectX 8 vertex buffers and sorting vertex buffers for rendering in the SAGE engine.

## Responsibilities
- Creates and manages vertex buffers (DX8 and sorting types)
- Provides locking mechanisms for vertex buffer access
- Tracks vertex buffer memory usage and statistics
- Handles dynamic vertex buffer allocation and reuse
- Supports various vertex formats (positions, normals, textures, etc.)

## Key Types
- VertexBufferClass (Class): Base class for vertex buffers
- DX8VertexBufferClass (Class): DirectX 8 vertex buffer implementation
- SortingVertexBufferClass (Class): Software vertex buffer for sorting
- DynamicVBAccessClass (Class): Manages dynamic vertex buffer access
- FVFInfoClass (Class): Flexible vertex format information

## Key Functions
### VertexBufferClass::WriteLockClass::WriteLockClass
- Purpose: Locks vertex buffer for writing
- Calls: DX8_Assert(), DX8_ErrorCode(), Get_DX8_Vertex_Buffer()->Lock()

### VertexBufferClass::AppendLockClass::AppendLockClass
- Purpose: Locks vertex buffer for appending data
- Calls: DX8_Assert(), DX8_ErrorCode(), Get_DX8_Vertex_Buffer()->Lock()

### DynamicVBAccessClass::Allocate_DX8_Dynamic_Buffer
- Purpose: Allocates or reuses a dynamic DX8 vertex buffer
- Calls: REF_PTR_RELEASE(), NEW_REF(), DX8VertexBufferClass constructor

### DynamicVBAccessClass::Allocate_Sorting_Dynamic_Buffer
- Purpose: Allocates or reuses a dynamic sorting vertex buffer
- Calls: REF_PTR_RELEASE(), NEW_REF(), SortingVertexBufferClass constructor

## Globals
- _DynamicSortingVertexArrayInUse (bool): Tracks if sorting vertex array is in use
- _DynamicDX8VertexBufferInUse (bool): Tracks if DX8 vertex buffer is in use
- _DynamicFVFInfo (FVFInfoClass): Default FVF info for dynamic buffers
- _DX8VertexBufferCount (int): Count of DX8 vertex buffers
- _VertexBufferCount (int): Total vertex buffer count
- _VertexBufferTotalVertices (int): Total vertices across all buffers
- _VertexBufferTotalSize (int): Total memory used by vertex buffers
- dx8_lock (int): Debug lock counter for DX8 operations

## Dependencies
- dx8vertexbuffer.h, dx8wrapper.h, dx8fvf.h, dx8caps.h, thread.h, wwmemlog.h
- D3dx8core.h (DirectX 8 SDK)
- W3D memory allocation functions (W3DNEW, W3DNEWARRAY)
- Reference counting macros (REF_PTR_SET, REF_PTR_RELEASE)
- Debug assertion macros (WWASSERT, DX8_Assert)
- DX8 error handling (DX8_ErrorCode)
