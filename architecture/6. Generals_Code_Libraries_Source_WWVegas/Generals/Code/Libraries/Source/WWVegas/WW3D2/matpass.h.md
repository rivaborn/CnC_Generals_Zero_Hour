# Generals/Code/Libraries/Source/WWVegas/WW3D2/matpass.h

## Purpose
Defines the MaterialPassClass for managing additional material passes for rendering effects in the SAGE engine.

## Responsibilities
- Wraps data for extra material passes (textures, shaders, materials)
- Manages culling volumes and per-polygon culling flags
- Provides accessors for texture/shader/material state
- Handles Direct3D material installation/cleanup

## Key Types
- **MaterialPassClass (Class)**: Manages material pass data for rendering effects.
- **TextureClass (Class)**: Reference to texture data (forward declared).
- **VertexMaterialClass (Class)**: Reference to vertex material data (forward declared).
- **MeshModelClass (Class)**: Reference to mesh model data (forward declared).
- **OBBoxClass (Class)**: Reference to culling volume data (forward declared).
- **MAX_TEX_STAGES (Enum)**: Defines maximum texture stages (2).

## Key Functions
### MaterialPassClass::Install_Materials
- Purpose: Installs materials into Direct3D state.
- Calls: Not inferable (virtual method).

### MaterialPassClass::Set_Texture
- Purpose: Sets a texture for a specific stage.
- Calls: Not inferable.

### MaterialPassClass::Set_Shader
- Purpose: Sets the shader for this material pass.
- Calls: Not inferable.

### MaterialPassClass::Set_Material
- Purpose: Sets the vertex material for this pass.
- Calls: Not inferable.

### MaterialPassClass::Peek_Texture
- Purpose: Safely retrieves a texture reference without null checks.
- Calls: WWASSERT (assertion).

## Globals
- **EnablePerPolygonCulling (static bool)**: Tracks per-polygon culling enable state.

## Dependencies
