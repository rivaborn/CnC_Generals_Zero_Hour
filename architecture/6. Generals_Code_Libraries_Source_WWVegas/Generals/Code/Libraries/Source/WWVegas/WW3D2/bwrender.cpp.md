# Generals/Code/Libraries/Source/WWVegas/WW3D2/bwrender.cpp

## Purpose
Implements a black-and-white 2D software renderer for triangle strips and triangles.

## Responsibilities
- Manages a pixel buffer for rendering
- Handles vertex transformations and culling
- Renders triangles and triangle strips using a preprocessed approach
- Provides methods for filling and clearing the buffer

## Key Types
- `Buffer` (Class): Manages the pixel buffer and its dimensions
- `BWRenderClass` (Class): Main renderer class handling triangle rendering

## Key Functions
### `Cull`
- Purpose: Determines if a triangle should be culled based on winding order
- Calls: None

### `Render_Triangle_Strip`
- Purpose: Renders a triangle strip with culling and preprocessing
- Calls: `Cull`, `Render_Preprocessed_Triangle`

### `Render_Triangles`
- Purpose: Renders individual triangles with culling and preprocessing
- Calls: `Cull`, `Render_Preprocessed_Triangle`

### `Render_Preprocessed_Triangle`
- Purpose: Renders a preprocessed triangle by scanning lines
- Calls: `pixel_buffer.Set_H_Line`

## Globals
- None

## Dependencies
- `bwrender.h`, `vp.h`
- `Vector2`, `Vector3`, `Vector3i`, `VectorProcessorClass`, `WWMath`
