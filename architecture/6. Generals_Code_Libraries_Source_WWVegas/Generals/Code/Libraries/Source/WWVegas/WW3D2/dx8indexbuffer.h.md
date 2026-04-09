# Generals/Code/Libraries/Source/WWVegas/WW3D2/dx8indexbuffer.h

## Purpose
Defines index buffer classes for Direct3D 8 rendering, including wrapper classes for dynamic and sorting buffers.

## Responsibilities
- Declares abstract `IndexBufferClass` and concrete implementations (`DX8IndexBufferClass`, `SortingIndexBufferClass`)
- Manages dynamic index buffer access via `DynamicIBAccessClass`
- Provides locking mechanisms for index buffer modification (`WriteLockClass`, `AppendLockClass`)
- Tracks engine references and buffer statistics

## Key Types
- **IndexBufferClass (Class)**: Abstract base class for index buffers.
- **DX8IndexBufferClass (Class)**: Wraps Direct3D 8 index buffers with usage flags.
- **SortingIndexBufferClass (Class)**: Manages sorting-specific index buffers.
- **DynamicIBAccessClass (Class)**: Handles dynamic index buffer allocation and recycling.
- **UsageType (Enum)**: Defines buffer usage types (default, dynamic, software processing, patches).

## Key Functions
### `IndexBufferClass::Copy`
- Purpose: Copies index data into the buffer.
- Calls: Not inferable (implementation in .cpp).

### `DynamicIBAccessClass::Allocate_Sorting_Dynamic_Buffer`
- Purpose: Allocates a sorting-specific dynamic buffer.
- Calls: Not inferable.

### `DynamicIBAccessClass::Allocate_DX8_Dynamic_Buffer`
- Purpose: Allocates a Direct3D 8 dynamic buffer.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `always.h`, `wwdebug.h`, `refcount.h`, `sphere.h`
- External classes: `DX8Wrapper`, `SortingRendererClass`
- External struct: `IDirect3DIndexBuffer8`
