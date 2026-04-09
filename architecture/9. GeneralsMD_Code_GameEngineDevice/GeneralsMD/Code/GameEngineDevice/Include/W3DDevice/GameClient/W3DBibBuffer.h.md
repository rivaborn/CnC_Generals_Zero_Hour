# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DBibBuffer.h

## Purpose
Manages a draw buffer for rendering "bibs" (decal-like objects) in a 3D scene.

## Responsibilities
- Stores and manages bib data (position, highlight state, color, etc.)
- Handles vertex/index buffer allocation and rendering
- Supports adding/removing bibs by object or drawable ID
- Tracks visibility and sorting state for optimization

## Key Types
- **TBib (struct)**: Represents a single bib with corners, highlight flag, color, and IDs
- **W3DBibBuffer (class)**: Main class managing the bib buffer system
- **INITIAL_BIB_VERTEX (enum)**: Initial vertex buffer size (256)
- **INITIAL_BIB_INDEX (enum)**: Initial index buffer size (384)
- **MAX_BIBS (enum)**: Maximum number of bibs (1000)

## Key Functions
### addBib/addBibDrawable
- Purpose: Adds a new bib to the buffer
- Calls: Not inferable (implementation in .cpp)

### removeBib/removeBibDrawable
- Purpose: Removes a bib from the buffer by ID
- Calls: Not inferable

### renderBibs
- Purpose: Renders all active bibs
- Calls: loadBibsInVertexAndIndexBuffers

### loadBibsInVertexAndIndexBuffers
- Purpose: Prepares vertex/index data for rendering
- Calls: Not inferable

## Globals
- None

## Dependencies
- **Includes**: rendobj.h, w3d_file.h, dx8vertexbuffer.h, dx8indexbuffer.h, shader.h, vertmaterial.h, BaseType.h, GameType.h, AsciiString.h
- **
