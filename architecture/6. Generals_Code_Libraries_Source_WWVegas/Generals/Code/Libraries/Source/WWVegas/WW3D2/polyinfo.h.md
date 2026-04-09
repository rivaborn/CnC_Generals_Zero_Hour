# Generals/Code/Libraries/Source/WWVegas/WW3D2/polyinfo.h

## Purpose
Header file defining a simple storage class for polygon rendering properties (texture, vertex material, shader).

## Responsibilities
- Stores references to rendering assets (texture, vertex material, shader)
- Provides getter/setter methods for these assets
- Manages lifetime of stored pointers

## Key Types
- **TextureClass (Class)**: Not inferable.
- **VertexMaterialClass (Class)**: Not inferable.
- **ShaderClass (Class)**: Not inferable.
- **PolygonInfoClass (Class)**: Stores polygon rendering properties (texture, vertex material, shader).

## Key Functions
### Peek_Texture
- Purpose: Returns the stored texture pointer.
- Calls: None.

### Peek_Vertex_Material
- Purpose: Returns the stored vertex material pointer.
- Calls: None.

### Peek_Shader
- Purpose: Returns the stored shader pointer.
- Calls: None.

### Set_Texture
- Purpose: Sets the texture pointer.
- Calls: None.

### Set_Vertex_Material
- Purpose: Sets the vertex material pointer.
- Calls: None.

### Set_Shader
- Purpose: Sets the shader pointer.
- Calls: None.

### Set
- Purpose: Sets all rendering properties at once.
- Calls: Set_Texture, Set_Vertex_Material, Set_Shader.

### PolygonInfoClass (constructor)
- Purpose: Initializes the polygon info with optional texture, vertex material, and shader.
- Calls: Set.

### ~PolygonInfoClass (destructor)
- Purpose: Cleans up the polygon info.
- Calls: None.

## Globals
None.

## Dependencies
- Key includes: None (forward declarations only).
- External symbols: TextureClass, VertexMaterialClass, ShaderClass.
