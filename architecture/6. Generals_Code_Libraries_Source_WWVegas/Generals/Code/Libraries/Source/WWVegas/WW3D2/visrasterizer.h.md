# Generals/Code/Libraries/Source/WWVegas/WW3D2/visrasterizer.h

## Purpose
Defines classes for visibility rasterization, including ID buffer management and triangle rendering for visibility precalculation.

## Responsibilities
- Manages ID buffer and Z buffer for visibility calculations
- Handles triangle rasterization and backface culling
- Provides pixel counter statistics for rendering
- Supports occluder/non-occluder rendering modes
- Manages model-view transformations for rendering

## Key Types
- **IDBufferClass (Class)**: Manages ID buffer and Z buffer, provides low-level rasterization
- **VisRasterizerClass (Class)**: Encapsulates visibility rasterization with model-view transformations
- **ModeType (Enum)**: Rendering mode (occluder/non-occluder)
- **CameraClass (Class)**: External camera reference (forward declared)
- **AABoxClass (Class)**: External bounding box reference (forward declared)
- **GradientsStruct (Struct)**: Gradient data for scanline rendering
- **EdgeStruct (Struct)**: Edge data for scanline rendering

## Key Functions
### IDBufferClass::Render_Triangle
- Purpose: Renders a triangle into the ID buffer
- Calls: Is_Backfacing, Render_Occluder_Scanline/Render_Non_Occluder_Scanline

### VisRasterizerClass::Render_Triangles
- Purpose: Renders multiple triangles with clipping
- Calls: Update_MV_Transform, Render_Triangles_Clip/Render_Triangles_No_Clip

### VisRasterizerClass::Update_MV_Transform
- Purpose: Updates model-view transformation matrix
- Calls: Not inferable (internal calculation)

## Globals
None

## Dependencies
- Key includes: "always.h", "matrix3d.h", "matrix4.h", "vector3i.h", "vector3.h", "simplevec.h", "bittype.h", "plane.h"
- External symbols: CameraClass, AABoxClass, GradientsStruct, EdgeStruct (forward declared)
