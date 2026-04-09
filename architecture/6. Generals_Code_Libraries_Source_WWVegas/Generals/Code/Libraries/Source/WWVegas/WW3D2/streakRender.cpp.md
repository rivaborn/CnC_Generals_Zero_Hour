# Generals/Code/Libraries/Source/WWVegas/WW3D2/streakRender.cpp

## Purpose
Handles rendering of streak effects (e.g., trails, beams) in the game using DirectX 8.

## Responsibilities
- Manages streak geometry subdivision and transformation
- Handles texture mapping and UV coordinate animation
- Processes line intersections and merging for proper rendering
- Configures shaders and rendering states for streak effects
- Supports chunked rendering for performance optimization

## Key Types
- **StreakRendererClass (Class)**: Main class for streak rendering functionality
- **StreakSubdivision (Struct)**: Helper struct for subdivision processing
- **LineSegmentIntersection (Struct)**: Represents intersection points between line segments
- **TextureMapMode (Enum)**: Defines different texture mapping modes

## Key Functions
### StreakRendererClass::RenderStreak
- Purpose: Renders a streak effect with specified points, colors, and widths
- Calls: DX8Wrapper::Get_Transform, DX8Wrapper::Set_Transform, VectorProcessorClass::Transform, SortingRendererClass::Insert_Triangles, DX8Wrapper::Draw_Triangles

### StreakRendererClass::subdivision_util
- Purpose: Performs subdivision on streak points for smoother rendering
- Calls: Random3Class operations, Vector3SolidBoxRandomizer operations

### StreakRendererClass::Init
- Purpose: Initializes streak renderer with properties from W3dEmitterLinePropertiesStruct
- Calls: Set_Merge_Intersections, Set_Freeze_Random, Set_Disable_Sorting, Set_End_Caps, Set_Texture_Mapping_Mode, etc.

## Globals
- **STREAK_CHUNK_SIZE (const)**: Defines chunk size for rendering optimization
- **MAX_STREAK_POINT_BUFFER_SIZE (const)**: Maximum buffer size for streak points
- **MAX_STREAK_POLY_BUFFER_SIZE (const)**: Maximum buffer size for streak polygons

## Dependencies
- streakrender.h
- ww3d.h
- rinfo.h
- dx8wrapper.h
- sortingrenderer.h
- vp.h
- vector3i.h
- random.h
- v3_rnd.h
- ShaderClass, TextureClass, VertexMaterialClass, DynamicVBAccessClass, DynamicIBAccessClass from external libraries
