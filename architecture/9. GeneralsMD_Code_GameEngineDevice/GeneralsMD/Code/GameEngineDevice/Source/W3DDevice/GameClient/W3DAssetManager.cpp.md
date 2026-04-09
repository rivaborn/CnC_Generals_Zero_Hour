# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DAssetManager.cpp

## Purpose
Manages 3D assets (textures, models) with Generals-specific extensions for team coloring and scaling.

## Responsibilities
- Handles texture and render object loading with caching
- Supports team-color recoloring and HSV-based color shifting
- Manages asset prototypes and unique instance creation
- Provides texture replacement functionality
- Integrates with Granny animation system

## Key Types
- **W3DPrototypeClass (Class)**: Wraps RenderObjClass prototypes for asset management
- **W3DPrototypeClassMagicEnum (Enum)**: Not inferable
- **W3DPrototypeClass_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### Munge_Render_Obj_Name
- Purpose: Generates unique names for scaled/colored render objects
- Calls: None

### Munge_Texture_Name
- Purpose: Generates unique names for recolored textures
- Calls: None

### Recolor_Texture_One_Time
- Purpose: Creates a new texture with HSV color shift applied
- Calls: SurfaceClass methods, TextureLoader::Request_High_Priority_Loading

### Recolor_Asset
- Purpose: Recursively recolors render objects based on HSV shift
- Calls: Recolor_Mesh, Recolor_HLOD, Recolor_ParticleEmitter

### Create_Render_Obj
- Purpose: Creates render objects with optional scaling and color shifting
- Calls: WW3DAssetManager::Create_Render_Obj, Find_Prototype, Make_Unique

## Globals
- **ident_scale (float)**: Identity scale value (1.0)
- **scale_epsilon (float)**: Tolerance for scale comparison
- **ident_HSV (Vector3)**: Identity HSV values (0,0,0)
- **H_epsilon/S_epsilon/V_epsilon (float)**: Tolerance for HSV comparisons
- **TEAM_COLOR_PALETTE_SIZE (int)**: Size of team color palette
- **houseColorScale (float)**: Scale factor for team colors

## Dependencies
- Key includes: "W3DDevice/GameClient/W3DAssetManager.h", "rendobj.h", "texture.h", "mesh.h", "hlod.h"
- External symbols: WW3DAssetManager methods, DX8Wrapper functions, GrannyAnimManagerClass
