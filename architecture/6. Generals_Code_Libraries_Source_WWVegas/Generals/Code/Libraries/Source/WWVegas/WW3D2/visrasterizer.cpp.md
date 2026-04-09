# Generals/Code/Libraries/Source/WWVegas/WW3D2/visrasterizer.cpp

## Purpose
Implements a visibility rasterizer for the SAGE engine, handling polygon clipping, triangle rendering, and depth-based occlusion testing.

## Responsibilities
- Polygon clipping against view frustum planes
- Triangle rasterization with depth testing
- Occlusion culling via ID buffer
- Camera/view transformation management

## Key Types
- **VisPolyClass (Class)**: Polygon clipping utility with vertex management
- **GradientsStruct (Struct)**: Computes 1/Z gradients for triangle edges
- **EdgeStruct (Struct)**: Handles scanline conversion of triangle edges
- **VisRasterizerClass (Class)**: Main rasterizer managing transformations and rendering
- **IDBufferClass (Class)**: Depth/ID buffer for occlusion testing

## Key Functions
### VisPolyClass::Clip
- Purpose: Clips polygon against a plane using Sutherland-Hodgman algorithm
- Calls: `plane.In_Front`, `plane.Compute_Intersection`, `Vector3::Lerp`

### VisRasterizerClass::Render_Triangles_Clip
- Purpose: Renders clipped triangles against view frustum
- Calls: `VisPolyClass::Clip`, `CameraClass::Project_Camera_Space_Point`, `IDBufferClass::Render_Triangle`

### IDBufferClass::Render_Triangle
- Purpose: Rasterizes a triangle with depth testing
- Calls: `Is_Backfacing`, `GradientsStruct::GradientsStruct`, `EdgeStruct::EdgeStruct`, `Render_Occluder_Scanline`/`Render_Non_Occluder_Scanline`

## Globals
- **_VisPoly0 (VisPolyClass)**: Temporary clipping polygon storage
- **_VisPoly1 (VisPolyClass)**: Temporary clipping polygon storage

## Dependencies
- `visrasterizer.h`, `camera.h`, `plane.h`, `vp.h`
- `Vector3`, `Matrix3D`, `Vector3i`, `AABoxClass`, `CollisionMath`, `VectorProcessorClass`, `WWMath`
