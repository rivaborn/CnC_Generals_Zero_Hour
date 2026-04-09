# Generals/Code/Libraries/Source/WWVegas/WW3D2/dx8indexbuffer.cpp

## Purpose
Manages DirectX 8 index buffers and sorting index buffers for 3D rendering in the SAGE engine.

## Responsibilities
- Creates and manages index buffers for GPU rendering
- Provides locking mechanisms for writing index data
- Handles dynamic index buffers for performance optimization
- Tracks buffer usage statistics
- Supports both DirectX 8 and software sorting index buffers

## Key Types
- **IndexBufferClass (Class)**: Base class for index buffers
- **DX8IndexBufferClass (Class)**: DirectX 8 specific index buffer implementation
- **SortingIndexBufferClass (Class)**: Software-based sorting index buffer
- **DynamicIBAccessClass (Class)**: Manages dynamic index buffer allocation
- **WriteLockClass (Class)**: RAII lock for writing to index buffers
- **AppendLockClass (Class)**: RAII lock for appending to index buffers

## Key Functions
### IndexBufferClass::Copy
- Purpose: Copies index data into the buffer
- Calls: DX8IndexBufferClass::AppendLockClass, DX8IndexBufferClass::WriteLockClass

### DynamicIBAccessClass::Allocate_DX8_Dynamic_Buffer
- Purpose: Allocates or reuses a dynamic DirectX 8 index buffer
- Calls: DX8IndexBufferClass constructor, REF_PTR_RELEASE, REF_PTR_SET

### DynamicIBAccessClass::Allocate_Sorting_Dynamic_Buffer
- Purpose: Allocates or reuses a dynamic sorting index buffer
- Calls: SortingIndexBufferClass constructor, REF_PTR_RELEASE, REF_PTR_SET

## Globals
- **_DynamicSortingIndexArrayInUse (bool)**: Tracks if dynamic sorting buffer is in use
- **_DynamicSortingIndexArray (SortingIndexBufferClass*)**: Pointer to dynamic sorting buffer
- **_DynamicSortingIndexArraySize (unsigned short)**: Size of dynamic sorting buffer
- **_DynamicSortingIndexArrayOffset (unsigned short)**: Current offset in sorting buffer
- **_DynamicDX8IndexBufferInUse (bool)**: Tracks if dynamic DX8 buffer is in use
- **_DynamicDX8IndexBuffer (DX8IndexBufferClass*)**: Pointer to dynamic DX8 buffer
- **_DynamicDX8IndexBufferSize (unsigned short)**: Size of dynamic DX8 buffer
- **_DynamicDX8IndexBufferOffset (unsigned short)**: Current offset in DX8 buffer
- **_IndexBufferCount (int)**: Total count of index buffers
- **_IndexBufferTotalIndices (int)**: Total indices across all buffers
- **_IndexBufferTotalSize (int)**: Total memory used by all buffers

## Dependencies
- dx8indexbuffer.h
- dx8wrapper.h
- dx8caps.h
- sphere.h
- thread.h
- DirectX 8 API (D3D)
- W3D memory allocation functions (W3DNEWARRAY)
