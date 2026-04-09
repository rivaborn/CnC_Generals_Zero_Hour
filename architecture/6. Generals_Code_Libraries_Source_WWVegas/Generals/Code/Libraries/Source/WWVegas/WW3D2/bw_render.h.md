# Generals/Code/Libraries/Source/WWVegas/WW3D2/bw_render.h

## Purpose
Declares the `BW_Render` class for software-based triangle rendering using a pixel buffer.

## Responsibilities
- Manages a pixel buffer for rendering triangles
- Provides methods for rendering triangles and triangle strips
- Handles vertex transformations and preprocessing

## Key Types
- `BW_Render` (Class): Main rendering class for software triangle rendering
- `Buffer` (Class): Internal pixel buffer helper class

## Key Functions
### `BW_Render::Render_Preprocessed_Triangle`
- Purpose: Renders a preprocessed triangle using the pixel buffer
- Calls: `Buffer::Set_H_Line`, `Buffer::Fill`

### `BW_Render::Fill`
- Purpose: Fills the entire buffer with a specified color
- Calls: `Buffer::Fill`

### `BW_Render::Set_Vertex_Locations`
- Purpose: Sets the vertex locations for rendering
- Calls: None

### `BW_Render::Render_Triangles`
- Purpose: Renders a list of triangles using indices
- Calls: `Render_Preprocessed_Triangle`

### `BW_Render::Render_Triangle_Strip`
- Purpose: Renders a triangle strip using indices
- Calls: `Render_Preprocessed_Triangle`

## Globals
- None

## Dependencies
- `always.h`, `vector2.h`, `vector3.h`, `vector3i.h`
- `Vector2`, `Vector3`, `Vector3i` (external types)
