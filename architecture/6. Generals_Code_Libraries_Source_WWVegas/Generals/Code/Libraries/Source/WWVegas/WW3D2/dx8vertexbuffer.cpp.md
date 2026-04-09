# Generals/Code/Libraries/Source/WWVegas/WW3D2/dx8vertexbuffer.cpp

## Purpose
Manages DirectX 8 vertex buffers and sorting vertex buffers for 3D rendering in the SAGE engine.

## Responsibilities
- Creates and manages vertex buffers (DX8 and sorting types)
- Provides locking mechanisms for vertex buffer access
- Tracks vertex buffer usage statistics
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

### DX8VertexBufferClass::Copy
- Purpose: Copies vertex data into the buffer
- Calls: VertexBufferClass::AppendLockClass, VertexBufferClass::WriteLockClass

### DynamicVBAccessClass::Allocate_DX8_Dynamic_Buffer
- Purpose: Allocates or reuses a dynamic DX8 vertex buffer
- Calls: REF_PTR_RELEASE(), NEW_REF(), DX8VertexBufferClass constructor

### DynamicVBAccessClass::WriteLockClass::WriteLockClass
- Purpose: Locks dynamic vertex buffer for writing
- Calls: DX8_Assert(), DX8_ErrorCode(), Get_DX8_Vertex_Buffer()->Lock()

## Globals
- _DynamicSortingVertexArrayInUse (bool): Tracks if sorting vertex array is in use
- _DynamicDX8VertexBuffer (DX8VertexBufferClass*): Global dynamic DX8 vertex buffer
- _DynamicDX8VertexBufferSize (unsigned short): Size of dynamic DX8 vertex buffer
- _DynamicDX8VertexBufferOffset (unsigned short): Current offset in dynamic DX8 buffer
- _DX8VertexBufferCount (int): Count of DX8 vertex buffers
- _VertexBufferCount (int): Total vertex buffer count
- _VertexBufferTotalVertices (int): Total vertices across all buffers
- _VertexBufferTotalSize (int): Total memory used by vertex buffers
- dx8_lock (int): Lock counter for DX8 operations

## Dependencies
- dx8vertexbuffer.h, dx8wrapper.h, dx8fvf.h, dx8caps.h, thread.h
- D3dx8core.h (DirectX 8 SDK)
- W3D memory allocation functions (W3DNEW, W3DNEWARRAY)
- Reference counting macros (REF_PTR_SET, REF_PTR_RELEASE)
- Debug assertion macros (WWASSERT, DX8_Assert)
