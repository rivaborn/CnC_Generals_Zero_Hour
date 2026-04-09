# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DWaterTracks.h

## Purpose
Manages water track/wave rendering objects and their lifecycle in the SAGE engine.

## Responsibilities
- Defines `WaterTracksObj` for animated water effects (waves/splashes)
- Implements `WaterTracksRenderSystem` to manage, update, and render water tracks
- Handles resource allocation/release for DirectX 8 vertex/index buffers
- Provides track binding/unbinding and state persistence (save/load)

## Key Types
- **waveType (Enum)**: Not inferable (forward reference only)
- **WaterTracksObj (Class)**: Represents a single water track/wave with animation state
- **WaterTracksRenderSystem (Class)**: Manages a pool of water track objects and rendering

## Key Functions
### WaterTracksObj::init
- Purpose: Allocates W3D resources and sets track dimensions/position
- Calls: Not inferable

### WaterTracksRenderSystem::flush
- Purpose: Renders all active water tracks in the current frame
- Calls: Not inferable

### WaterTracksRenderSystem::update
- Purpose: Updates animation state (alpha fading, removal) for all tracks
- Calls: Not inferable

### WaterTracksRenderSystem::bindTrack
- Purpose: Acquires a free water track object for use
- Calls: Not inferable

## Globals
- **m_vertexBuffer (DX8VertexBufferClass)**: Vertex buffer for track rendering
- **m_indexBuffer (DX8IndexBufferClass)**: Index buffer defining track triangles
- **m_usedModules (WaterTracksObj*)**: Linked list of active tracks
- **m_freeModules (WaterTracksObj*)**: Linked list of reusable tracks

## Dependencies
- DX8VertexBufferClass, DX8IndexBufferClass, VertexMaterialClass, Shader
