# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DGranny.cpp

## Purpose
Handles integration of Granny 3D models into the W3D rendering engine for Command & Conquer Generals.

## Responsibilities
- Manages Granny model instances and animations
- Handles model rendering with proper transformations and scaling
- Implements collision detection for Granny models
- Manages render state batching for performance
- Provides interface between Granny API and W3D engine

## Key Types
- GrannyRenderObjClass (Class): Represents a renderable Granny model instance
- GrannyRenderObjSystem (Class): Manages batching and rendering of multiple Granny objects
- GrannyPrototypeClass (Class): Contains prototype data for Granny models

## Key Functions
### GrannyRenderObjClass::Render
- Purpose: Renders the Granny model using W3D rendering pipeline
- Calls: TheGrannyRenderObjSystem->AddRenderObject, GrannySetModelClock, GrannySampleModelAnimations, GrannyBuildModelWorldTransforms

### GrannyRenderObjSystem::AddRenderObject
- Purpose: Adds a Granny render object to the batching system for deferred rendering
- Calls: None visible in this file

### GrannyRenderObjSystem::Flush
- Purpose: Renders all batched Granny objects with optimized state changes
- Calls: GrannySetModelClock, GrannySampleModelAnimations, GrannyBuildModelWorldTransforms, DX8Wrapper rendering functions

## Globals
- g_blendingBuffer (granny_pnt332_vertex[4096]): Temporary workspace for vertex deformation
- TheGrannyRenderObjClassSystem (GrannyRenderObjClassSystem*): Singleton instance of the Granny render system

## Dependencies
- Granny SDK (granny2.lib)
- W3D engine components (WW3D2/DX8Wrapper.h, WW3D2/Scene.h)
- Game engine systems (assetmgr.h, camera.h, texture.h)
- Common utilities (colmath.h, rinfo.h)
