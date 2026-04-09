# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DAssetManager.h

## Purpose
Manages 3D assets (models, textures, animations) for the W3D rendering system in Generals/Zero Hour.

## Responsibilities
- Loads and creates 3D render objects
- Manages textures and animations
- Handles asset recoloring and texture replacement
- Reports used assets for debugging

## Key Types
- **W3DAssetManager (Class)**: Main asset manager for W3D assets
- **Vector3 (Class)**: 3D vector type
- **VertexMaterialClass (Class)**: Vertex material data
- **GrannyAnimManagerClass (Class)**: Animation manager

## Key Functions
### Create_Render_Obj
- Purpose: Creates a render object from a file
- Calls: Not inferable

### Get_Texture
- Purpose: Loads a texture with specified parameters
- Calls: Not inferable

### Recolor_Asset
- Purpose: Recolors a render object
- Calls: Recolor_Mesh, Recolor_HLOD, Recolor_Vertex_Material

### replacePrototypeTexture
- Purpose: Replaces textures in a render object prototype
- Calls: Not inferable

## Globals
- **m_GrannyAnimManager (GrannyAnimManagerClass*)**: Animation manager instance

## Dependencies
- assetmgr.h
- Lib/BaseType.h
- WW3DAssetManager (base class)
- RenderObjClass, HAnimClass, TextureClass (external)
