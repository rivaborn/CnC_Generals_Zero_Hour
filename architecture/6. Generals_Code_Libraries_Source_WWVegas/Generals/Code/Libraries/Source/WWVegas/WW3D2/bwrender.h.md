# Generals/Code/Libraries/Source/WWVegas/WW3D2/bwrender.h

## Purpose
Header for a black-and-white triangle rasterizer used to generate shadow textures.

## Responsibilities
- Defines `BWRenderClass` for fast software rendering without z-buffering or texturing
- Manages pixel buffer and vertex rendering
- Provides triangle rendering methods (indexed and strip)

## Key Types
- **BWRenderClass (Class)**: Main renderer class for black-and-white triangles
- **Buffer (Class)**: Internal pixel buffer wrapper with scaling and fill operations

## Key Functions
### `BWRenderClass::Render_Preprocessed_Triangle`
- Purpose: Renders a preprocessed triangle into the buffer
- Calls: `pixel_buffer.Set_H_Line`

### `BWRenderClass::Render_Triangles`
- Purpose: Renders triangles using indexed vertices
- Calls: `Render_Preprocessed_Triangle`

### `BWRenderClass::Render_Triangle_Strip`
- Purpose: Renders a triangle strip
- Calls: `Render_Preprocessed_Triangle`

## Globals
- None

## Dependencies
- `always.h`, `vector2.h`, `vector3.h`, `vector3i.h`
- Uses `Vector2`, `Vector3`, `Vector3i` types
