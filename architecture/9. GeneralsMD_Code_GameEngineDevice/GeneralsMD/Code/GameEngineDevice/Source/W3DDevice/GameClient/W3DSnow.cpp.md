# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DSnow.cpp

## Purpose
Manages snow particle rendering in the game using Direct3D 8.

## Responsibilities
- Initializes and releases snow rendering resources
- Updates snow particle positions based on time and camera movement
- Renders snow particles using either point sprites or quads depending on hardware support
- Handles frustum culling to optimize performance

## Key Types
- POINTVERTEX (Struct): Contains a Vector3 representing the center of a snow particle
- W3DSnowManager (Class): Manages snow rendering (not shown in symbols but is the main class)

## Key Functions
### FtoDW
- Purpose: Converts a float to a DWORD for Direct3D render state parameters
- Calls: None

### renderSubBox
- Purpose: Recursively subdivides the snow rendering area for frustum culling
- Calls: CollisionMath::Overlap_Test, renderSubBox (recursive)

### render
- Purpose: Main entry point for rendering snow particles
- Calls: renderAsQuads, renderSubBox, DX8Wrapper functions, TheTerrainRenderObject->getMaximumVisibleBox

### renderAsQuads
- Purpose: Renders snow particles as quads when point sprites are not supported
- Calls: DX8Wrapper functions, DynamicVBAccessClass methods

## Globals
- SNOW_BUFFER_SIZE (const int): Size of vertex buffer for particles (4096)
- SNOW_BATCH_SIZE (const int): Maximum particles rendered per draw call (2048)
- D3DFVF_POINTVERTEX (const int): Vertex format flag for point vertices

## Dependencies
- W3DSnow.h (header)
- heightmap.h
- View.h
- dx8wrapper.h
- rinfo.h
- camera.h
- assetmgr.h
- Direct3D 8 API (via DX8Wrapper)
- WWMath, CollisionMath, WW3D, Debug_Statistics classes
