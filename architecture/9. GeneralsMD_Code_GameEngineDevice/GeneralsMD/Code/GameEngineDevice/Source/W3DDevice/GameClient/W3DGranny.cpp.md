# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DGranny.cpp

## Purpose
Handles integration of Granny 3D models into the W3D rendering engine for Command & Conquer Generals.

## Responsibilities
- Manages Granny model instances and animations
- Handles rendering of skinned meshes with proper transformations
- Implements collision detection for Granny models
- Provides a system for batching render objects by material
- Manages texture binding and vertex buffer updates

## Key Types
- `GrannyRenderObjClass` (Class): Represents a renderable Granny model instance
- `GrannyRenderObjSystem` (Class): Manages batching and rendering of multiple Granny objects
- `GrannyPrototypeClass` (Class): Contains prototype data for Granny models
- `granny_pnt332_vertex` (Struct): Vertex format used for Granny mesh deformation

## Key Functions
### `GrannyRenderObjClass::Render`
- Purpose: Adds the object to the render system's batch for deferred rendering
- Calls: `TheGrannyRenderObjSystem->AddRenderObject`

### `GrannyRenderObjSystem::AddRenderObject`
- Purpose: Batches render objects by material/prototype for efficient rendering
- Calls: Granny material/texture queries, vertex/index buffer management

### `GrannyRenderObjSystem::Flush`
- Purpose: Renders all batched Granny objects with proper state sorting
- Calls: Granny animation sampling, DX8Wrapper rendering calls

### `GrannyRenderObjClass::Set_Animation`
- Purpose: Configures animation playback for a Granny model
- Calls: `GrannyPlayControlledAnimation`, `GrannySetControlSpeed`

## Globals
- `g_blendingBuffer` (granny_pnt332_vertex[4096]): Temporary workspace for mesh deformation
- `TheGrannyRenderObjClassSystem` (GrannyRenderObjSystem*): Singleton instance of the render system

## Dependencies
- Granny SDK (granny2.lib)
- W3D engine components (WW3D2/DX8Wrapper.h, Scene.h)
- Asset management (assetmgr.h)
- Rendering infrastructure (texture.h, colmath.h)
- Global game data (common/GlobalData.h)
