# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DAssetManager.cpp

## Purpose
Manages 3D assets (textures, models, prototypes) for the W3D rendering system in Command & Conquer Generals.

## Responsibilities
- Loads and caches textures and render objects
- Handles asset recoloring and scaling
- Manages prototype instances and asset modifications
- Supports team color tinting and HSV color shifts

## Key Types
- **W3DPrototypeClass (Class)**: Wraps render object prototypes for instantiation
- **W3DPrototypeClassMagicEnum (Enum)**: Not inferable
- **W3DPrototypeClass_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### Get_Texture
- Purpose: Retrieves or creates a texture by filename
- Calls: TextureHash.Get, NEW_REF, TextureLoader::Request_High_Priority_Loading

### Create_Render_Obj
- Purpose: Creates a render object with optional scaling and HSV shifting
- Calls: Find_Prototype, Load_3D_Assets, Make_Unique, Recolor_Asset

### Recolor_Texture_One_Time
- Purpose: Applies HSV color shift to a texture
- Calls: TextureLoader::Request_High_Priority_Loading, SurfaceClass methods

### Munge_Render_Obj_Name
- Purpose: Generates unique names for scaled/colored asset variants
- Calls: None

## Globals
- **ident_scale (float)**: Identity scale value (1.0)
- **scale_epsilon (float)**: Tolerance for scale comparison
- **ident_HSV (Vector3)**: Identity HSV values
- **H_epsilon/S_epsilon/V_epsilon (float)**: Tolerance for HSV comparisons
- **TEAM_COLOR_PALETTE_SIZE (Int)**: Size of team color palette (16)
- **houseColorScale (UnsignedShort[])**: Array of color scale values

## Dependencies
- Key includes: "W3DDevice/GameClient/W3DAssetManager.h", "proto.h", "rendobj.h", "texture.h"
- External symbols: SurfaceClass methods, DX8Wrapper functions, WWPROFILE/WWMEMLOG macros
