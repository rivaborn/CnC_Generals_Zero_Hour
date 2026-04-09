# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/Shadow/W3DVolumetricShadow.cpp

## Purpose
Implements volumetric shadow rendering using shadow volumes for the SAGE engine.

## Responsibilities
- Manages shadow volume geometry creation and rendering
- Handles dynamic and static shadow volumes
- Optimizes shadow volume updates based on light/object movement
- Manages D3D vertex/index buffers for shadow rendering
- Provides geometry caching and loading system

## Key Types
- **SHADOW_STATIC_VOLUME_VERTEX (struct)**: Vertex structure for static shadow volumes
- **SHADOW_DYNAMIC_VOLUME_VERTEX (struct)**: Vertex structure for dynamic shadow volumes
- **Geometry (struct)**: Generic geometry container with visibility state tracking
- **W3DShadowGeometryMesh (class)**: Mesh-specific shadow geometry data
- **W3DShadowGeometryManager (class)**: Manages cached shadow geometries
- **VisibleState (enum)**: Tracks polygon visibility state (STATE_UNKNOWN/STATE_VISIBLE/STATE_INVISIBLE)

## Key Functions
### W3DVolumetricShadowManager::addShadow
- Purpose: Adds a shadow caster to the shadow management system
- Calls: Get_Geom, Load_Geom, setRenderObject, SetGeometry, setRenderObjExtent, setShadowLengthScale

### W3DVolumetricShadowManager::ReAcquireResources
- Purpose: Reallocates D3D resources after device reset
- Calls: ReleaseResources, CreateIndexBuffer, CreateVertexBuffer, ReAcquireResources (W3DBufferManager)

### W3DShadowGeometryManager::Load_Geom
- Purpose: Loads shadow geometry from a W3D RenderObject
- Calls: initFromHLOD, initFromMesh, Peek_Geom, Add_Geom

## Globals
- **TheW3DVolumetricShadowManager (W3DVolumetricShadowManager*)**: Global shadow manager instance
- **shadowCameraFrustum (const FrustumClass*)**: Frustum for shadow camera culling
- **cosAngleToCare (Real)**: Threshold for shadow volume updates based on light movement
- **shadowVertexBufferD3D (LPDIRECT3DVERTEXBUFFER8)**: D3D vertex buffer for shadows
- **shadowIndexBufferD3D (LPDIRECT3DINDEXBUFFER8)**: D3D index buffer for shadows

## Dependencies
- Direct3D 8 (DX8Wrapper)
- W3D rendering system (RenderObjClass, MeshClass, HLodClass)
- Math libraries (Vector3, AABoxClass, SphereClass)
- Game-specific systems (TerrainLogic, Drawable)
- HashTableClass for geometry caching
