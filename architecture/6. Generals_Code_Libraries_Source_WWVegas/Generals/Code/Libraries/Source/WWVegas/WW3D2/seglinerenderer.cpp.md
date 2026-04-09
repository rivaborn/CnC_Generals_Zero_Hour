# Generals/Code/Libraries/Source/WWVegas/WW3D2/seglinerenderer.cpp

## Purpose
Implements a segmented line renderer for the SAGE engine, handling textured, width-adjusted lines with subdivision and intersection merging.

## Responsibilities
- Renders 3D lines with configurable width, texture, and opacity
- Handles recursive subdivision for fractal noise effects
- Manages intersection merging and edge plane calculations
- Supports UV offset animation and multiple texture mapping modes
- Integrates with the sorting renderer for translucent lines

## Key Types
- **SegLineRendererClass** (Class): Main renderer class for segmented lines
- **TextureMapMode** (Enum): Texture mapping modes (UNIFORM_WIDTH, UNIFORM_LENGTH, TILED)
- **LineSegment** (Struct): Represents a line segment with start plane and edge planes
- **LineSegmentIntersection** (Struct): Stores intersection data for merging logic

## Key Functions
### `Render`
- Purpose: Renders a segmented line with given points and transform
- Calls: `subdivision_util`, `DX8Wrapper::Get_Transform`, `DX8Wrapper::Set_Transform`, `SortingRendererClass::Insert_Triangles`, `DX8Wrapper::Draw_Triangles`

### `subdivision_util`
- Purpose: Recursively subdivides line segments with fractal noise
- Calls: `Random3Class`, `Vector3SolidBoxRandomizer::Get_Vector`

### `Init`
- Purpose: Initializes renderer from emitter line properties
- Calls: None (setter methods)

## Globals
- **SEGLINE_CHUNK_SIZE** (const): Chunk size for processing points
- **MAX_SEGLINE_POINT_BUFFER_SIZE** (const): Maximum points buffer size
- **MAX_SEGLINE_POLY_BUFFER_SIZE** (const): Maximum polygon buffer size

## Dependencies
- `seglinerenderer.h`, `ww3d.h`, `rinfo.h`, `dx8wrapper.h`, `sortingrenderer.h`, `vp.h`, `vector3i.h`, `random.h`, `v3_rnd.h`
- `TextureClass`, `ShaderClass`, `VertexMaterialClass`, `DynamicVBAccessClass`, `DynamicIBAccessClass`, `SphereClass`, `Matrix3D`, `Matrix4`, `Vector3`, `Vector2`
