# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/polyinfo.h

## Purpose
Defines a simple storage class for polygon rendering state, tracking texture, vertex material, and shader.

## Responsibilities
- Stores references to rendering assets (texture, vertex material, shader)
- Provides getter/setter methods for these assets
- Initializes and cleans up stored references

## Key Types
- **TextureClass (Class)**: Reference to a texture asset
- **VertexMaterialClass (Class)**: Reference to a vertex material asset
- **ShaderClass (Class)**: Reference to a shader asset
- **PolygonInfoClass (Class)**: Container for polygon rendering state

## Key Functions
### Peek_Texture / Peek_Vertex_Material / Peek_Shader
- Purpose: Get const references to stored assets
- Calls: None

### Set_Texture / Set_Vertex_Material / Set_Shader
- Purpose: Set references to rendering assets
- Calls: None

### Set
- Purpose: Set all three rendering assets at once
- Calls: Set_Texture, Set_Vertex_Material, Set_Shader

### PolygonInfoClass (constructor)
- Purpose: Initialize with optional texture, vertex material, and shader
- Calls: Set

### ~PolygonInfoClass (destructor)
- Purpose: Clean up stored references
- Calls: None

## Globals
- None

## Dependencies
- Forward declarations: TextureClass, VertexMaterialClass, ShaderClass
- No external symbols used
