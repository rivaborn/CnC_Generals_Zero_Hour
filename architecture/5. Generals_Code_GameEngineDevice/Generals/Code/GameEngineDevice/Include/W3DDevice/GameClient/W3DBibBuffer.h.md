# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DBibBuffer.h

## Purpose
Manages a buffer for rendering "bibs" (decal-like objects) in the 3D scene.

## Responsibilities
- Stores and manages bib data (position, highlight state, color, etc.)
- Handles vertex/index buffer allocation and loading for rendering
- Provides methods to add/remove bibs and clear the buffer
- Renders bibs with optional highlighting

## Key Types
- **TBib (struct)**: Represents a single bib with corners, highlight flag, color, and IDs.
- **W3DBibBuffer (class)**: Main class managing the bib buffer and rendering.
- **MeshClass (class)**: Forward-declared dependency for mesh operations.

## Key Functions
### `addBib`
- Purpose: Adds a bib to the buffer at specified corners.
- Calls: None visible.

### `removeBib`
- Purpose: Removes a bib by its ObjectID.
- Calls: None visible.

### `renderBibs`
- Purpose: Renders all bibs in the buffer.
- Calls: `loadBibsInVertexAndIndexBuffers`.

### `loadBibsInVertexAndIndexBuffers`
- Purpose: Prepares vertex/index buffers for rendering.
- Calls: None visible.

## Globals
- **INITIAL_BIB_VERTEX (enum)**: Initial vertex buffer size (256).
- **INITIAL_BIB_INDEX (enum)**: Initial index buffer size (384).
- **MAX_BIBS (enum)**: Maximum number of bibs (1000).

## Dependencies
- `DX8VertexBufferClass`, `DX8IndexBufferClass`, `TextureClass`, `Vector3`
- `ObjectID`, `DrawableID`, `Bool`, `Int` from base types
- DirectX
