# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dx8vertexbuffer.h

## Purpose
Defines vertex buffer classes for DirectX 8 rendering, including dynamic and sorting buffers.

## Responsibilities
- Wraps DirectX 8 vertex buffers
- Manages dynamic vertex buffer access
- Provides locking mechanisms for vertex buffer modification
- Supports different vertex formats and usage types

## Key Types
- **VertexBufferClass (Class)**: Base class for vertex buffers, provides reference counting and basic interface.
- **DX8VertexBufferClass (Class)**: DirectX 8 vertex buffer implementation with various constructors for different vertex formats.
- **SortingVertexBufferClass (Class)**: Special vertex buffer for alpha-sorted rendering.
- **DynamicVBAccessClass (Class)**: Manages access to recycled dynamic vertex buffers.
- **UsageType (Enum)**: Defines vertex buffer usage types (default, dynamic, software processing, n-patches).

## Key Functions
### VertexBufferClass::WriteLockClass::WriteLockClass
- Purpose: Locks vertex buffer for writing.
- Calls: Not inferable.

### VertexBufferClass::AppendLockClass::AppendLockClass
- Purpose: Locks vertex buffer for appending vertices.
- Calls: Not inferable.

### DynamicVBAccessClass::WriteLockClass::WriteLockClass
- Purpose: Locks dynamic vertex buffer for writing.
- Calls: Not inferable.

### DX8VertexBufferClass::Create_Vertex_Buffer
- Purpose: Creates the underlying DirectX 8 vertex buffer.
- Calls: Not inferable.

## Globals
- **dynamic_fvf_type (unsigned)**: Defines the default flexible vertex format for dynamic buffers.

## Dependencies
- Key includes: "always.h", "wwdebug.h", "refcount.h", "dx8fvf.h"
- External symbols: D3DFVF_* flags, IDirect3DVertexBuffer8 interface
