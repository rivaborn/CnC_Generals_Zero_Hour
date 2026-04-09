# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DCustomEdging.h

## Purpose
Manages rendering of tree-like objects (edging) in the 3D scene using vertex and index buffers.

## Responsibilities
- Allocates and manages vertex/index buffers for edging geometry
- Handles adding, clearing, and drawing edging objects
- Performs visibility culling based on camera position
- Updates edging data when view changes

## Key Types
- **W3DCustomEdging (Class)**: Main class handling edging rendering
- **WorldHeightMap (Class)**: Reference to height map data (external)
- **(anonymous enum)**: Contains buffer size constants
- **MAX_EDGE_VERTEX (Enum)**: Maximum vertex count (4Ã2000)
- **MAX_EDGE_INDEX (Enum)**: Maximum index count (6Ã2000)

## Key Functions
### W3DCustomEdging::addEdging
- Purpose: Adds a new edging object with position, scale, and rotation
- Calls: None (direct)

### W3DCustomEdging::drawEdging
- Purpose: Renders visible edging objects within view frustum
- Calls: loadEdgingsInVertexAndIndexBuffers

### W3DCustomEdging::allocateEdgingBuffers
- Purpose: Initializes vertex and index buffers
- Calls: None (direct)

### W3DCustomEdging::loadEdgingsInVertexAndIndexBuffers
- Purpose: Loads edging data into GPU buffers for rendering
- Calls: None (direct)

## Globals
- **MAX_BLENDS (const)**: Maximum number of edging objects (2000)

## Dependencies
- DirectX 8 vertex/index buffer classes
- W3D file system and rendering objects
- Shader and material
