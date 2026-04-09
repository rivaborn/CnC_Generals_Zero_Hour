# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/matpass.h

## Purpose
Defines the MaterialPassClass for managing additional material passes for rendering effects in the SAGE engine.

## Responsibilities
- Wraps data for extra material passes (textures, shaders, materials)
- Manages texture stages, culling volumes, and per-polygon culling
- Provides accessors for material pass properties
- Handles Direct3D state installation/cleanup

## Key Types
- **MaterialPassClass (Class)**: Manages material pass data for rendering effects.
- **TextureClass (Class)**: Reference to texture data (forward declared).
- **VertexMaterialClass (Class)**: Reference to vertex material data (forward declared).
- **MeshModelClass (Class)**: Reference to mesh model data (forward declared).
- **OBBoxClass (Class)**: Reference to culling volume data (forward declared).
- **MAX_TEX_STAGES (Enum)**: Defines maximum texture stages (8).

## Key Functions
### MaterialPassClass::Install_Materials
- Purpose: Installs Direct3D materials and states.
- Calls: Not inferable (virtual method).

### MaterialPassClass::Set_Texture
- Purpose: Sets a texture for a specific stage.
- Calls: Not inferable.

### MaterialPassClass::Set_Shader
- Purpose: Sets a shader for the material pass.
- Calls: Not inferable.

### MaterialPassClass::Set_Material
- Purpose: Sets a vertex material for the pass.
- Calls: Not inferable.

### MaterialPassClass::Peek_Texture
- Purpose: Retrieves a texture without refcounting.
- Calls: WWASSERT (assertion).

## Globals
- **EnablePerPolygonCulling (static bool)**: Tracks per-polygon culling state.

## Dependencies
-
