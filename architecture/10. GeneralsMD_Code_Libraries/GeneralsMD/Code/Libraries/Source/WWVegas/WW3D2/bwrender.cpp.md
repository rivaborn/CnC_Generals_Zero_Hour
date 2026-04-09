# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/bwrender.cpp

## Purpose
Implements a basic 2D software rasterizer for rendering triangles and triangle strips using a simple buffer.

## Responsibilities
- Manages a pixel buffer for rendering
- Handles vertex transformations and culling
- Renders triangles and triangle strips via scanline algorithm
- Provides buffer manipulation utilities (fill, horizontal lines)

## Key Types
- `Buffer` (Class): Manages a 2D pixel buffer with scaling and clipping
- `BWRenderClass` (Class): Main renderer class handling triangle rendering
- `Cull` (Function): Static culling function for backface elimination

## Key Functions
### `Cull`
- Purpose: Determines if a triangle should be culled based on winding order
- Calls: None

### `Render_Triangle_Strip`
- Purpose: Renders a triangle strip with backface culling
- Calls: `Cull`, `Render_Preprocessed_Triangle`

### `Render_Triangles`
- Purpose: Renders individual triangles with backface culling
- Calls: `Cull`, `Render_Preprocessed_Triangle`

### `Render_Preprocessed_Triangle`
- Purpose: Renders a pre-sorted triangle using scanline algorithm
- Calls: `pixel_buffer.Set_H_Line`, `WWMath::Float_To_Long`

## Globals
- None

## Dependencies
- `bwrender.h`, `vp.h`, `<string.h>`
- `Vector2`, `Vector3`, `Vector3i`, `VectorProcessorClass`, `WWMath`
