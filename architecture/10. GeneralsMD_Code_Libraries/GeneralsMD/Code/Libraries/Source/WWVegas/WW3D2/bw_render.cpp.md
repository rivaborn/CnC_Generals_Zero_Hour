# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/bw_render.cpp

## Purpose
Implements a basic 2D software rasterizer for rendering triangles and triangle strips using a pixel buffer.

## Responsibilities
- Manages a pixel buffer for rendering
- Handles vertex transformations and culling
- Renders triangles and triangle strips via scanline algorithm
- Provides buffer manipulation utilities (fill, horizontal lines)

## Key Types
- `Buffer` (Class): Wraps a pixel buffer with clipping and drawing operations
- `BW_Render` (Class): Main rasterizer class handling triangle rendering
- `Cull` (Function): Static inline function for back-face culling

## Key Functions
### `Cull`
- Purpose: Determines if a triangle should be culled based on winding order
- Calls: None

### `Render_Triangle_Strip`
- Purpose: Renders a triangle strip with back-face culling and scanline rasterization
- Calls: `Cull`, `Render_Preprocessed_Triangle`

### `Render_Triangles`
- Purpose: Renders individual triangles with back-face culling and scanline rasterization
- Calls: `Cull`, `Render_Preprocessed_Triangle`

### `Render_Preprocessed_Triangle`
- Purpose: Rasterizes a pre-sorted triangle using a two-pass scanline algorithm
- Calls: `Buffer::Set_H_Line`, `WWMath::Float_To_Long`

## Globals
- None

## Dependencies
- `bw_render.h` (header)
- `vp.h` (VectorProcessorClass)
- `WWMath` (for float-to-long conversion)
- `Vector2`, `Vector3`, `Vector3i` (math types)
- `memset` (C runtime)
