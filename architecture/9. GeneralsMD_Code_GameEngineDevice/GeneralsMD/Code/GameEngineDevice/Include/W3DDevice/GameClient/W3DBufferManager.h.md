# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DBufferManager.h

## Purpose
Manages partial vertex and index buffer allocations for Direct3D rendering.

## Responsibilities
- Allocates and recycles vertex/index buffer slots
- Tracks buffer usage and free memory
- Handles resource release/acquisition for D3D
- Provides buffer iteration capabilities

## Key Types
- **W3DBufferManager (Class)**: Main buffer management class
- **VBM_FVF_TYPES (Enum)**: Vertex format definitions
- **W3DRenderTask (Struct)**: Rendering task container
- **W3DVertexBufferSlot (Struct)**: Vertex buffer slot metadata
- **W3DVertexBuffer (Struct)**: Vertex buffer container
- **W3DIndexBufferSlot (Struct)**: Index buffer slot metadata
- **W3DIndexBuffer (Struct)**: Index buffer container

## Key Functions
### getSlot
- Purpose: Retrieves a free vertex/index buffer slot
- Calls: allocateSlotStorage

### ReleaseResources
- Purpose: Releases D3D/W3D resources
- Calls: Not inferable

### ReAcquireResources
- Purpose: Reacquires D3D/W3D resources
- Calls: Not inferable

### getNextVertexBuffer
- Purpose: Iterates over vertex buffers of specific type
- Calls: None

## Globals
- **TheW3DBufferManager (W3DBufferManager*)**: Singleton instance

## Dependencies
- dx8vertexbuffer.h
- dx8indexbuffer.h
- BaseType.h
