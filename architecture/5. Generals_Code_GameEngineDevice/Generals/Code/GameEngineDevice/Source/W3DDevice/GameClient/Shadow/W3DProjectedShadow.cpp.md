# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/Shadow/W3DProjectedShadow.cpp

## Purpose
Manages projected shadows in the game, including texture generation and rendering for shadow effects.

## Responsibilities
- Manages shadow textures and their rendering
- Handles projection of shadows onto terrain
- Updates shadow textures when lights or objects move
- Maintains shadow vertex/index buffers for rendering

## Key Types
- **SHADOW_DECAL_VERTEX (struct)**: Vertex structure for shadow decals with position, color, and texture coordinates
- **W3DProjectedShadow (class)**: Represents a projected shadow for a render object
- **W3DShadowTexture (class)**: Manages shadow texture data and bounds
- **W3DShadowTextureManager (class)**: Manages a collection of shadow textures
- **W3DShadowTextureManagerIterator (class)**: Iterator for shadow texture manager

## Key Functions
### W3DProjectedShadow::updateTexture
- Purpose: Updates the shadow texture based on light position and object type
- Calls: m_shadowProjector->Compute_Perspective_Projection, m_shadowProjector->Compute_Texture, m_shadowTexture[0]->updateBounds

### W3DProjectedShadow::updateProjectionParameters
- Purpose: Recomputes projection matrix when light or object moves
- Calls: m_shadowProjector->Pre_Render_Update

### W3DProjectedShadowManager::renderProjectedTerrainShadow
- Purpose: Renders shadow on terrain covered by a world-space bounding box
- Calls: DX8Wrapper::Draw_Indexed_Primitive, DX8Wrapper::Set_Texture

### W3DShadowTexture::updateBounds
- Purpose: Updates the bounding volume of the shadow based on light position
- Calls: robj->Get_Bounding_Box, robj->Get_Position

## Globals
- **TheW3DProjectedShadowManager (W3DProjectedShadowManager*)**: Global singleton for shadow management
- **shadowDecalVertexBufferD3D (LPDIRECT3DVERTEXBUFFER8)**: D3D vertex buffer for shadow decals
- **shadowDecalIndexBufferD3D (LPDIRECT3DINDEXBUFFER8)**: D3D index buffer for shadow decals
- **drawEdgeX/drawEdgeY/drawStartX/drawStartY (Int)**: Bounding rectangle for rendered terrain portion

## Dependencies
- Direct3D 8 interfaces (LPDIRECT3DVERTEXBUFFER8, LPDIRECT3DINDEXBUFFER8)
- W3D engine classes (RenderObjClass, TextureClass, CameraClass)
- Math libraries (Matrix3D, Vector3, AABoxClass)
- Game-specific classes (W3DShadowManager, SpecialRenderInfoClass)
- HashTableClass for texture management
