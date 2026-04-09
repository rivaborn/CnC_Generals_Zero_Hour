# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/bwrender.h

## Purpose
Header for a black-and-white triangle rasterizer used to generate shadow textures.

## Responsibilities
- Defines `BWRenderClass` for fast software rendering of triangles
- Manages an internal pixel buffer for rendering
- Provides methods for rendering triangles and triangle strips
- Supports vertex location setting and buffer filling

## Key Types
- **BWRenderClass (Class)**: Main renderer class for black-and-white triangle rasterization
- **Buffer (Class)**: Internal pixel buffer management class

## Key Functions
### BWRenderClass::Render_Preprocessed_Triangle
- Purpose: Renders a preprocessed triangle
- Calls: `pixel_buffer.Set_H_Line`, `pixel_buffer.Fill`

### BWRenderClass::Fill
- Purpose: Fills the buffer with a specified value
- Calls: `pixel_buffer.Fill`

### BWRenderClass::Set_Vertex_Locations
- Purpose: Sets vertex locations for rendering
- Calls: None

### BWRenderClass::Render_Triangles
- Purpose: Renders triangles using index data
- Calls: `Render_Preprocessed_Triangle`

### BWRenderClass::Render_Triangle_Strip
- Purpose: Renders a triangle strip using index data
- Calls: `Render_Preprocessed_Triangle`

### Buffer::Set_H_Line
- Purpose: Sets a horizontal line in the buffer
- Calls: None

### Buffer::Fill
- Purpose: Fills the buffer with a value
- Calls: None

## Globals
- None

## Dependencies
- `always.h`, `vector2.h`, `vector3.h`, `vector3i.h`
- `Vector2`, `Vector3`, `Vector3i`
