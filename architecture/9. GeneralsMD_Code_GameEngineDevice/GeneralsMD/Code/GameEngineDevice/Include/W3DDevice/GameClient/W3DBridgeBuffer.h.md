# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DBridgeBuffer.h

## Purpose
Header file defining bridge rendering system for the SAGE engine, including bridge geometry, culling, and buffer management.

## Responsibilities
- Defines bridge types and rendering data structures
- Manages bridge vertex/index buffers
- Handles bridge visibility culling
- Provides bridge loading and rendering interface

## Key Types
- **W3DBridge (Class)**: Individual bridge representation with geometry and state
- **W3DBridgeBuffer (Class)**: Manages collection of bridges and rendering buffers
- **TBridgeType (Enum)**: Bridge type classification (fixed/sectional)
- **BodyDamageType (Enum)**: Bridge damage states
- **BridgeInfo (Class)**: Bridge metadata container

## Key Functions
### W3DBridge::getModelVertices
- Purpose: Extracts vertex data from mesh for bridge rendering
- Calls: Not inferable (mesh access methods)

### W3DBridgeBuffer::drawBridges
- Purpose: Renders all visible bridges
- Calls: cull(), loadBridgesInVertexAndIndexBuffers()

### W3DBridgeBuffer::loadBridges
- Purpose: Loads bridges from map data
- Calls: addBridge()

## Globals
- **MAX_BRIDGE_VERTEX (const)**: Maximum vertices per bridge (12000)
- **MAX_BRIDGE_INDEX (const)**: Maximum indices per bridge (24000)
- **MAX_BRIDGES (const)**: Maximum bridges in buffer (200)

## Dependencies
- DirectX 8 vertex/index buffer classes
- W3D rendering primitives (MeshClass, TextureClass)
- Math types (Vector3, Matrix3D)
- Game engine types (CameraClass, Dict)
