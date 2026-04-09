# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DBridgeBuffer.h

## Purpose
Defines bridge rendering infrastructure for the W3D engine, including bridge objects and their buffer management.

## Responsibilities
- Manages bridge geometry and rendering
- Handles bridge visibility culling
- Maintains vertex/index buffers for bridge rendering
- Provides bridge loading and initialization
- Supports bridge damage states

## Key Types
- **W3DBridge (Class)**: Represents individual bridge objects with geometry and state
- **W3DBridgeBuffer (Class)**: Manages collection of bridges and their rendering
- **TBridgeType (Enum)**: Bridge type classification (fixed/sectional)
- **BodyDamageType (Enum)**: Bridge damage state enumeration
- **BridgeInfo (Class)**: Bridge information structure

## Key Functions
### W3DBridge::getModelVertices
- Purpose: Extracts vertex data from bridge mesh models
- Calls: Not inferable

### W3DBridgeBuffer::drawBridges
- Purpose: Renders all active bridges in the buffer
- Calls: Not inferable

### W3DBridgeBuffer::loadBridges
- Purpose: Loads bridges from map objects
- Calls: Not inferable

## Globals
- **MAX_BRIDGE_VERTEX (Enum)**: Maximum vertices per bridge buffer
- **MAX_BRIDGE_INDEX (Enum)**: Maximum indices per bridge buffer
- **MAX_BRIDGES (Enum)**: Maximum number of bridges

## Dependencies
- `MeshClass`, `W3DTerrainLogic`, `W3DAssetManager`, `SimpleSceneClass`
- DirectX 8 vertex/index buffer classes
- W3D rendering infrastructure
- Common game types and utilities
