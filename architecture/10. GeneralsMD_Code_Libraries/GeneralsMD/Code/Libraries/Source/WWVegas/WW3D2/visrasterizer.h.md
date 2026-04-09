# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/visrasterizer.h

## Purpose
Defines classes for ID buffer and visibility rasterization in the SAGE engine.

## Responsibilities
- Manages ID buffer and Z buffer for visibility precalculation
- Handles triangle rasterization and backface culling
- Provides interface for setting render modes and IDs
- Supports two-sided rendering and pixel counting

## Key Types
- **IDBufferClass (Class)**: Manages ID buffer and Z buffer, provides rasterization.
- **VisRasterizerClass (Class)**: Encapsulates ID buffer rasterization for visibility system.
- **ModeType (Enum)**: Render modes (OCCLUDER_MODE, NON_OCCLUDER_MODE).
- **CameraClass (Class)**: External camera reference.
- **AABoxClass (Class)**: External bounding box reference.
- **GradientsStruct (Struct)**: Not inferable.
- **EdgeStruct (Struct)**: Not inferable.

## Key Functions
### IDBufferClass::Render_Triangle
- Purpose: Renders a triangle into the ID buffer.
- Calls: Is_Backfacing, Render_Occluder_Scanline/Render_Non_Occluder_Scanline

### VisRasterizerClass::Render_Triangles
- Purpose: Renders triangles with clipping or without.
- Calls: Update_MV_Transform, Render_Triangles_Clip/Render_Triangles_No_Clip

### VisRasterizerClass::Set_Model_Transform
- Purpose: Sets the model/world transform matrix.
- Calls: None

### VisRasterizerClass::Set_Camera
- Purpose: Sets the camera reference.
- Calls: None

## Globals
- None

## Dependencies
- Key includes: "always.h", "matrix3d.h", "matrix4.h", "vector3i.h", "vector3.h", "simplevec.h", "bittype.h", "plane.h", "meshgeometry.h"
- External symbols: CameraClass, AABoxClass, GradientsStruct, EdgeStruct, TriIndex, WWASSERT
