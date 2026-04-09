# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dx8indexbuffer.h

## Purpose
Defines index buffer classes for Direct3D 8 rendering, including wrapper classes for DX8 and sorting buffers.

## Responsibilities
- Declares abstract `IndexBufferClass` and concrete implementations (`DX8IndexBufferClass`, `SortingIndexBufferClass`).
- Manages dynamic index buffer access via `DynamicIBAccessClass`.
- Provides locking mechanisms (`WriteLockClass`, `AppendLockClass`) for buffer modification.
- Tracks engine references and buffer statistics.

## Key Types
- **IndexBufferClass (Class)**: Abstract base class for index buffers.
- **DX8IndexBufferClass (Class)**: Wraps Direct3D 8 index buffers with usage flags.
- **SortingIndexBufferClass (Class)**: Manages sorting-specific index buffers.
- **DynamicIBAccessClass (Class)**: Handles dynamic index buffer allocation and recycling.
- **UsageType (Enum)**: Defines buffer usage types (default, dynamic, software processing, patches).

## Key Functions
### `IndexBufferExceptionFunc`
- Purpose: Exception handler for index buffer operations.
- Calls: Not inferable.

## Globals
- **IndexBufferExceptionFunc (Function)**: Global exception handler.

## Dependencies
- `always.h`, `wwdebug.h`, `refcount.h`, `sphere.h`
- `DX8Wrapper`, `SortingRendererClass`, `IDirect3DIndexBuffer8` (external classes/structs).
