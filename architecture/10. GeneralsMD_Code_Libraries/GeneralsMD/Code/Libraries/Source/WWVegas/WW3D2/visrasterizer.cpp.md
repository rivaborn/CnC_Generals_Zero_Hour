# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/visrasterizer.cpp

## Purpose
Implements a visibility rasterizer for the SAGE engine, handling polygon clipping, triangle rendering, and depth testing.

## Responsibilities
- Clips polygons against view frustum planes
- Renders triangles with depth testing (occluder/non-occluder modes)
- Manages ID and Z buffers for visibility determination
- Transforms vertices into screen space
- Handles backface culling

## Key Types
- **VisPolyClass (Class)**: Polygon clipping structure with vertex management
- **GradientsStruct (Struct)**: Computes gradients for triangle scan conversion
- **EdgeStruct (Struct)**: Handles edge scan conversion with 1/Z interpolation
- **VisRasterizerClass (Class)**: Main rasterizer class (defined elsewhere)
- **IDBufferClass (Class)**: ID/Z buffer management (defined elsewhere)

## Key Functions
### VisPolyClass::Clip
- Purpose: Clips a polygon against a plane
- Calls: `plane.In_Front`, `plane.Compute_Intersection`, `Vector3::Lerp`

### IDBufferClass::Render_Triangle
- Purpose: Renders a triangle with depth testing
- Calls: `Is_Backfacing`, `GradientsStruct` constructor, `EdgeStruct` constructor, `Render_Occluder_Scanline`/`Render_Non_Occluder_Scanline`

### IDBufferClass::Render_Occluder_Scanline
- Purpose: Renders a scanline for occluder mode (depth writes)
- Calls: `Pixel_Coords_To_Address`, `WWMath::Float_To_Long`, `WWMath::Ceil`, `WWMath::Max`

### IDBufferClass::Render_Non_Occluder_Scanline
- Purpose: Renders a scanline for non-occluder mode (depth test only)
- Calls: `Pixel_Coords_To_Address`, `WWMath::Float_To_Long`, `WWMath::Ceil`, `WWMath::Max`

## Globals
- **_VisPoly0 (VisPolyClass)**: Temporary clipping polygon storage
- **_VisPoly1 (VisPolyClass)**: Temporary clipping polygon storage

## Dependencies
- `visrasterizer.h`, `camera.h`, `plane.h`, `vp.h`
- `Vector3`, `Matrix3D`, `TriIndex`, `AABoxClass`, `CollisionMath`, `VectorProcessorClass`, `WWMath`
