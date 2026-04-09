# Generals/Code/Libraries/Source/WWVegas/WW3D2/dx8vertexbuffer.h

## Purpose
Defines vertex buffer classes for DirectX 8 rendering, including dynamic and sorting buffers.

## Responsibilities
- Wraps DirectX 8 vertex buffers (IDirect3DVertexBuffer8)
- Provides locking mechanisms for vertex buffer modification
- Manages dynamic vertex buffers for performance
- Supports different vertex formats (XYZNDUV2, etc.)
- Tracks engine references for resource management

## Key Types
- **VertexBufferClass (Class)**: Base class for vertex buffers, handles ref counting and basic operations.
- **DX8VertexBufferClass (Class)**: DirectX 8 specific vertex buffer implementation with usage types.
- **SortingVertexBufferClass (Class)**: Specialized buffer for alpha-sorted rendering.
- **DynamicVBAccessClass (Class)**: Manages recycled dynamic vertex buffers for efficiency.
- **UsageType (Enum)**: Defines vertex buffer usage flags (DEFAULT, DYNAMIC, etc.).
- **VertexBufferLockClass (Class)**: Base class for vertex buffer locks (write/append).
- **WriteLockClass (Class)**: Lock for writing to vertex buffers.
- **AppendLockClass (Class)**: Lock for appending to vertex buffers.

## Key Functions
### DynamicVBAccessClass::WriteLockClass::Get_Formatted_Vertex_Array
- Purpose: Returns pointer to writable vertex array with format validation.
- Calls: None (inline assertion only).

### DX8VertexBufferClass::Copy (variants)
- Purpose: Copies vertex data into the buffer.
- Calls: None (direct memory operations).

## Globals
- **dynamic_fvf_type (unsigned)**: Predefined FVF for dynamic buffers (XYZ|NORMAL|TEX2|DIFFUSE).

## Dependencies
- Key includes: "always.h", "wwdebug.h", "refcount.h", "dx8fvf.h"
- External symbols: D3DFVF_* flags, IDirect3DVertexBuffer8, Vector2/3/4, StringClass, FVFInfoClass.
