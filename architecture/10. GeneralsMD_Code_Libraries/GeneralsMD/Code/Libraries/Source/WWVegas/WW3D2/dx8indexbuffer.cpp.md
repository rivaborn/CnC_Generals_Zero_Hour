# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dx8indexbuffer.cpp

## Purpose
Manages DirectX 8 index buffers and sorting index buffers for 3D rendering in the SAGE engine.

## Responsibilities
- Creates and manages DX8 and sorting index buffers
- Provides locking mechanisms for writing to index buffers
- Tracks global index buffer statistics
- Handles dynamic index buffer allocation and reuse
- Manages reference counting for buffer objects

## Key Types
- **IndexBufferClass (Class)**: Base class for index buffers (DX8 and sorting types)
- **DX8IndexBufferClass (Class)**: DirectX 8 index buffer implementation
- **SortingIndexBufferClass (Class)**: CPU-side sorting index buffer
- **DynamicIBAccessClass (Class)**: Handles dynamic index buffer allocation and reuse
- **WriteLockClass (Class)**: RAII lock for writing to index buffers
- **AppendLockClass (Class)**: RAII lock for appending to index buffers

## Key Functions
### IndexBufferClass::Copy
- Purpose: Copies index data into the buffer
- Calls: DX8IndexBufferClass::AppendLockClass, DX8IndexBufferClass::WriteLockClass

### DynamicIBAccessClass::Allocate_DX8_Dynamic_Buffer
- Purpose: Allocates or reuses a dynamic DX8 index buffer
- Calls: DX8IndexBufferClass constructor, REF_PTR_RELEASE, REF_PTR_SET

### DynamicIBAccessClass::Allocate_Sorting_Dynamic_Buffer
- Purpose: Allocates or reuses a dynamic sorting index buffer
- Calls: SortingIndexBufferClass constructor, REF_PTR_RELEASE, REF_PTR_SET

### IndexBufferExceptionFunc
- Purpose: Prevents compiler optimization of exception handling code
- Calls: None

## Globals
- **_DynamicSortingIndexArrayInUse (bool)**: Tracks if dynamic sorting buffer is in use
- **_DynamicSortingIndexArray (SortingIndexBufferClass*)**: Global dynamic sorting buffer
- **_DynamicSortingIndexArraySize (unsigned short)**: Size of dynamic sorting buffer
- **_DynamicSortingIndexArrayOffset (unsigned short)**: Current offset in sorting buffer
- **_DynamicDX8IndexBufferInUse (bool)**: Tracks if dynamic DX8 buffer is in use
- **_DynamicDX8IndexBuffer (DX8IndexBufferClass*)**: Global dynamic DX8 buffer
- **_DynamicDX8IndexBufferSize (unsigned short)**: Size of dynamic DX8 buffer
- **_DynamicDX8IndexBufferOffset (unsigned short)**: Current offset in DX8 buffer
- **_IndexBufferCount (int)**: Total count of index buffers
- **_IndexBufferTotalIndices (int)**: Total indices across all buffers
- **_IndexBufferTotalSize (int)**: Total memory used by all buffers

## Dependencies
- dx8indexbuffer.h, dx8wrapper.h, dx8caps.h, sphere.h, thread.h, wwmemlog.h
- D3D device functions (CreateIndexBuffer, Lock, Unlock)
- WW3D, TextureClass, REF_PTR macros
