# Generals/Code/Libraries/Source/WWVegas/WW3D2/polyinfo.cpp

## Purpose
Manages polygon rendering information, including textures, vertex materials, and shaders.

## Responsibilities
- Handles reference counting for textures and vertex materials
- Manages shader allocation and cleanup
- Provides setters for polygon rendering properties

## Key Types
- `PolygonInfoClass` (Class): Contains polygon rendering state (texture, vertex material, shader)

## Key Functions
### `Set_Texture`
- Purpose: Sets the texture for the polygon and manages reference counting
- Calls: `Add_Ref()`, `Release_Ref()`

### `Set_Vertex_Material`
- Purpose: Sets the vertex material for the polygon and manages reference counting
- Calls: `Add_Ref()`, `Release_Ref()`

### `Set_Shader`
- Purpose: Sets the shader for the polygon (note: not reference-counted yet)
- Calls: `W3DNEW` (operator new)

### `~PolygonInfoClass`
- Purpose: Destructor that cleans up resources
- Calls: `Release_Ref()`, `delete`

## Globals
None

## Dependencies
- `polyinfo.h`, `texture.h`, `vertmaterial.h`, `shader.h`
- `TextureClass`, `VertexMaterialClass`, `ShaderClass`
