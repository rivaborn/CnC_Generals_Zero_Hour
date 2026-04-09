# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/FlatHeightMap.h

## Purpose
Defines a custom render object for terrain rendering and intersection tests in the SAGE engine.

## Responsibilities
- Manages terrain rendering, lighting, and scorchmarks
- Handles resource allocation and cleanup for heightmap data
- Processes camera movement and terrain LOD adjustments
- Supports partial updates and static lighting changes

## Key Types
- **FlatHeightMapRenderObjClass (Class)**: Custom W3D render object for terrain processing.
- **W3DTerrainBackground (Class)**: Pointer to terrain background data.
- **STATE_IDLE/STATE_MOVING/STATE_MOVING2/STATE_UPDATE_TEXTURES (Enum)**: States for terrain update logic.

## Key Functions
### FlatHeightMapRenderObjClass()
- Purpose: Constructor for the terrain render object.
- Calls: None

### Render()
- Purpose: Renders the terrain.
- Calls: Not inferable

### On_Frame_Update()
- Purpose: Updates terrain state per frame.
- Calls: Not inferable

### initHeightData()
- Purpose: Allocates resources for heightmap rendering.
- Calls: Not inferable

### freeMapResources()
- Purpose: Frees resources used for heightmap rendering.
- Calls: releaseTiles()

### updateCenter()
- Purpose: Updates terrain visibility based on camera position.
- Calls: Not inferable

### adjustTerrainLOD()
- Purpose: Adjusts terrain level of detail.
- Calls: Not inferable

### staticLightingChanged()
- Purpose: Handles changes in static lighting.
- Calls: Not inferable

### doPartialUpdate()
- Purpose: Updates a partial region of the terrain.
- Calls: Not inferable

### releaseTiles()
- Purpose: Releases terrain tiles.
- Calls: Not
