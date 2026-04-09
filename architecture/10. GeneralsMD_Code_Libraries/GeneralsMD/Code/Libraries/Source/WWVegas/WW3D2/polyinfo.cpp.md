# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/polyinfo.cpp

## Purpose
Manages polygon rendering information, including textures, vertex materials, and shaders.

## Responsibilities
- Handles reference counting for textures and vertex materials
- Manages shader allocation/deallocation
- Provides setters for polygon rendering properties

## Key Types
- `PolygonInfoClass` (Class): Container for polygon rendering state (texture, vertex material, shader)

## Key Functions
### `Set_Texture`
- Purpose: Assigns a texture to the polygon, managing reference counts
- Calls: `Add_Ref()`, `Release_Ref()`

### `Set_Vertex_Material`
- Purpose: Assigns a vertex material to the polygon, managing reference counts
- Calls: `Add_Ref()`, `Release_Ref()`

### `Set_Shader`
- Purpose: Assigns a shader to the polygon (note: not reference-counted yet)
- Calls: `W3DNEW` (for ShaderClass allocation)

### `~PolygonInfoClass`
- Purpose: Destructor that cleans up referenced objects
- Calls: `Release_Ref()`, `delete` (for Shader)

## Globals
None

## Dependencies
- `polyinfo.h`, `texture.h`, `vertmaterial.h`, `shader.h`
- `TextureClass`, `VertexMaterialClass`, `ShaderClass`
