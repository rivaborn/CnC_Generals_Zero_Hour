# Generals/Code/Libraries/Source/WWVegas/WW3D2/bw_render.cpp

## Purpose
Implements a basic 2D software rasterizer for rendering triangles and triangle strips.

## Responsibilities
- Manages a pixel buffer for rendering
- Handles vertex transformations and culling
- Renders triangles and triangle strips using a preprocessed approach
- Provides methods for filling and clearing the buffer

## Key Types
- `Buffer` (Class): Manages the pixel buffer and provides methods for setting horizontal lines and filling the buffer.
- `BW_Render` (Class): Main class for rendering operations, including setting vertex locations and rendering triangles.

## Key Functions
### `Cull`
- Purpose: Determines if a triangle should be culled based on winding order.
- Calls: None

### `Render_Triangle_Strip`
- Purpose: Renders a triangle strip from a list of indices.
- Calls: `Cull`, `Render_Preprocessed_Triangle`

### `Render_Triangles`
- Purpose: Renders individual triangles from a list of indices.
- Calls: `Cull`, `Render_Preprocessed_Triangle`

### `Render_Preprocessed_Triangle`
- Purpose: Renders a preprocessed triangle by setting horizontal lines in the buffer.
- Calls: `Set_H_Line`

## Globals
- None

## Dependencies
- `bw_render.h`: Header file for the BW_Render class.
- `vp.h`: Likely contains VectorProcessorClass and related utilities.
- `string.h`: For memset function.
- `Vector2`, `Vector3`, `Vector3i`: Vector classes used for vertex and coordinate storage.
- `WWMath::Float_To_Long`: Conversion utility for floating-point to integer coordinates.
