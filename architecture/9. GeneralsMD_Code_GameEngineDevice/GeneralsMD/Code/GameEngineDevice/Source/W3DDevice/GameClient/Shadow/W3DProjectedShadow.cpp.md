# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Shadow/W3DProjectedShadow.cpp

## Purpose
Manages projected shadows in the W3D rendering system, including texture generation and rendering.

## Responsibilities
- Manages shadow textures and their caching
- Handles shadow projection onto terrain
- Updates shadow textures based on light positions
- Manages shadow vertex/index buffers
- Provides shadow rendering functionality

## Key Types
- **SHADOW_DECAL_VERTEX (struct)**: Vertex structure for shadow decals (x,y,z,diffuse,u,v)
- **W3DShadowTexture (class)**: Manages individual shadow textures and their properties
- **W3DShadowTextureManager (class)**: Manages collection of shadow textures
- **W3DShadowTextureManagerIterator (class)**: Iterator for shadow texture manager
- **MissingTextureClass (class)**: Tracks missing textures to avoid repeated searches

## Key Functions
### W3DProjectedShadowManager::init
- Purpose: Initializes the shadow manager and its resources
- Calls: NEW, NEW_REF, SpecialRenderInfoClass constructor

### W3DProjectedShadowManager::ReAcquireResources
- Purpose: Recreates D3D resources after device reset
- Calls: DX8Wrapper::Create_Render_Target, CreateIndexBuffer, CreateVertexBuffer

### W3DProjectedShadow::updateTexture
- Purpose: Updates shadow texture based on light position
- Calls: TexProjectClass methods, SurfaceClass::Copy

### W3DShadowTextureManager::createTexture
- Purpose: Creates a new shadow texture from a render object
- Calls: NEW, W3DShadowTexture::init, addTexture

### W3DShadowTexture::updateBounds
- Purpose: Calculates shadow bounds based on light position
- Calls: RenderObjClass methods, AABoxClass::Init

## Globals
- **TheW3DProjectedShadowManager (W3DProjectedShadowManager*)**: Global singleton instance
- **TheProjectedShadowManager (ProjectedShadowManager*)**: Simplified global interface
- **shadowCameraFrustum (const FrustumClass*)**: Shadow camera frustum
- **shadowDecalVertexBufferD3D (LPDIRECT3DVERTEXBUFFER8)**: D3D vertex buffer for decals
- **shadowDecalIndexBufferD3D (LPDIRECT3DINDEXBUFFER8)**: D3D index buffer for decals
- **SHADOW_DECAL_VERTEX_SIZE (int)**: Size of decal vertex buffer
- **SHADOW_DECAL_INDEX_SIZE (int)**: Size of decal index buffer

## Dependencies
- WW3D2 headers (Camera, Light, DX8Wrapper, etc.)
- W3DDevice headers (W3DGranny, Heightmap, etc.)
- GameLogic headers (Object, PartitionManager)
- Common headers (GlobalData, Debug)
- Direct3D 8 interfaces
- D3dx8math library
