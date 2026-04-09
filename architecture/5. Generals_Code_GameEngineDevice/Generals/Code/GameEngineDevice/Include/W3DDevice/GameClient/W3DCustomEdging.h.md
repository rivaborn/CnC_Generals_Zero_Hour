# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DCustomEdging.h

## Purpose
Manages rendering of tree-like objects (edging) in the 3D scene using vertex and index buffers.

## Responsibilities
- Allocates and manages vertex/index buffers for edging geometry
- Handles adding, clearing, and drawing edging objects
- Performs visibility culling based on camera position
- Updates edging data when view changes

## Key Types
- **W3DCustomEdging (Class)**: Main class handling tree rendering
- **WorldHeightMap (Class)**: Reference to heightmap data (external)
- **(anonymous enum)**: Contains buffer size constants
- **MAX_EDGE_VERTEX (Enum)**: Maximum vertex count (4Ã2000)
- **MAX_EDGE_INDEX (Enum)**: Maximum index count (6Ã2000)

## Key Functions
### W3DCustomEdging::addEdging
- Purpose: Adds a new edging object to the buffer
- Calls: Not inferable

### W3DCustomEdging::drawEdging
- Purpose: Renders all edging objects with visibility culling
- Calls: loadEdgingsInVertexAndIndexBuffers

### W3DCustomEdging::allocateEdgingBuffers
- Purpose: Allocates vertex and index buffers
- Calls: Not inferable

### W3DCustomEdging::loadEdgingsInVertexAndIndexBuffers
- Purpose: Loads edging data into GPU buffers
- Calls: Not inferable

## Globals
- **MAX_BLENDS (const)**: Maximum number of edging objects (2000)

## Dependencies
- DirectX 8 vertex/index buffer classes
- W3D rendering system headers
- Common game types and string classes
