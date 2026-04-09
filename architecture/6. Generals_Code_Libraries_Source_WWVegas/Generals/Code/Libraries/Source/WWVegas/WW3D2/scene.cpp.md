# Generals/Code/Libraries/Source/WWVegas/WW3D2/scene.cpp

## Purpose
Manages scene rendering, object visibility, and scene state serialization in the WW3D2 engine.

## Responsibilities
- Base scene management (SceneClass)
- Simple scene implementation (SimpleSceneClass)
- Render object visibility culling
- Scene state serialization (save/load)
- Iterator support for scene traversal

## Key Types
- SceneClass (Class): Base scene management class
- SimpleSceneClass (Class): Concrete scene implementation
- SimpleSceneIterator (Class): Iterator for scene traversal
- (anonymous enum) (Enum): Chunk IDs for scene serialization

## Key Functions
### SceneClass::Render
- Purpose: Prepares scene for rendering with fog and extra pass handling
- Calls: DX8Wrapper::Set_Fog, Customized_Render

### SimpleSceneClass::Visibility_Check
- Purpose: Determines visibility of render objects using frustum culling
- Calls: CameraClass::Cull_Sphere, RenderObjClass::Prepare_LOD

### SimpleSceneClass::Customized_Render
- Purpose: Renders all visible objects in the scene
- Calls: Visibility_Check, RenderObjClass::Render, DX8Wrapper::Set_Light

### SimpleSceneClass::Compute_Point_Visibility
- Purpose: Tests point visibility via ray casting against scene objects
- Calls: RayCollisionTestClass operations, RenderObjClass::Cast_Ray

## Globals
None

## Dependencies
- scene.h, plane.h, camera.h, ww3d.h, rinfo.h, chunkio.h, dx8renderer.h, dx8wrapper.h, sortingrenderer.h, coltest.h
- DX8Wrapper, WW3D, WWDEBUG_SAY, WWASSERT, W3DNEW
