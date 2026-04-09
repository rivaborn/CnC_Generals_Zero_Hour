# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Shadow/W3DVolumetricShadow.cpp

## Purpose
Implements real-time volumetric shadow rendering using shadow volumes in the SAGE engine.

## Responsibilities
- Manages shadow volume geometry creation and rendering
- Handles dynamic and static shadow volume generation
- Optimizes shadow volume updates based on light/object movement
- Manages D3D vertex/index buffers for shadow rendering
- Provides shadow geometry caching system

## Key Types
- **Geometry (Struct)**: Holds shadow volume vertices, polygons, and visibility state
- **W3DShadowGeometryMesh (Class)**: Stores mesh-specific shadow data and neighbor info
- **W3DShadowGeometry (Class)**: Manages shadow geometry for render objects
- **W3DVolumetricShadowManager (Class)**: Central manager for all shadow volumes
- **VisibleState (Enum)**: Tracks polygon visibility state (STATE_UNKNOWN/STATE_VISIBLE/STATE_INVISIBLE)

## Key Functions
### W3DVolumetricShadowManager::addShadow
- Purpose: Adds a shadow caster to the shadow management system
- Calls: Get_Geom, Load_Geom, setRenderObject, SetGeometry, setRenderObjExtent, setShadowLengthScale

### W3DVolumetricShadowManager::ReAcquireResources
- Purpose: Reallocates D3D resources after device reset
- Calls: ReleaseResources, CreateIndexBuffer, CreateVertexBuffer, ReAcquireResources (W3DBufferManager)

### W3DShadowGeometryManager::Load_Geom
- Purpose: Creates shadow geometry from a W3D RenderObject
- Calls: initFromHLOD, initFromMesh, Add_Geom, Release_Ref

## Globals
- **TheW3DVolumetricShadowManager (W3DVolumetricShadowManager*)**: Singleton shadow manager instance
- **shadowCameraFrustum (const FrustumClass*)**: Frustum for shadow camera culling
- **cosAngleToCare (Real)**: Threshold for shadow volume updates based on light movement
- **shadowVertexBufferD3D/LPDIRECT3DVERTEXBUFFER8**: D3D vertex buffer for shadow rendering
- **shadowIndexBufferD3D/LPDIRECT3DINDEXBUFFER8**: D3D index buffer for shadow rendering

## Dependencies
- Direct3D 8 (DX8Wrapper)
- W3D rendering system (RenderObjClass, MeshClass, HLodClass)
- SAGE engine utilities (HashTableClass, StringClass)
- Math libraries (Vector3, AABoxClass, SphereClass)
- Game-specific systems (Drawable, TerrainLogic)
