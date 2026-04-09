# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/scene.cpp

## Purpose
Implements the scene management system for the W3D engine, handling render objects, visibility checks, and scene rendering.

## Responsibilities
- Manages render objects in a scene
- Handles visibility checks and LOD preparation
- Implements scene rendering with fog and lighting
- Provides iteration over render objects
- Saves/loads scene state via chunk system

## Key Types
- `(anonymous enum)` (Enum): Chunk ID constants for scene variables
- `SimpleSceneIterator` (Class): Iterator for traversing render objects in a scene

## Key Functions
### `SceneClass::Render`
- Purpose: Prepares scene for rendering and handles extra pass rendering modes
- Calls: `Pre_Render_Processing`, `DX8Wrapper::Set_Fog`, `Customized_Render`, `Post_Render_Processing`

### `SimpleSceneClass::Visibility_Check`
- Purpose: Determines visibility of render objects using frustum culling
- Calls: `CameraClass::Cull_Sphere`, `RenderObjClass::Prepare_LOD`

### `SimpleSceneClass::Customized_Render`
- Purpose: Renders all visible objects in the scene with lighting
- Calls: `Visibility_Check`, `DX8Wrapper::Set_Light`, `RenderObjClass::Render`

### `SimpleSceneClass::Post_Render_Processing`
- Purpose: Cleans up objects marked for release after rendering
- Calls: `RenderObjClass::Remove`, `RefRenderObjListClass::Release_Head`

## Globals
- None

## Dependencies
- `scene.h`, `plane.h`, `camera.h`, `ww3d.h`, `rinfo.h`, `chunkio.h`, `dx8renderer.h`, `dx8wrapper.h`, `sortingrenderer.h`, `coltest.h`
