# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DWater.h

## Purpose
Defines the water rendering system for the SAGE engine, handling various water types, reflections, and dynamic water effects.

## Responsibilities
- Manages water surface rendering (flat, reflective, shader-based, 3D mesh)
- Handles water physics (velocity, height changes, grid transformations)
- Controls sky/cloud rendering for reflections
- Provides water height queries for game logic
- Supports special water effects (rivers, wakes)

## Key Types
- **WaterRenderObjClass (Class)**: Main water rendering object with multiple water types.
- **WaterType (Enum)**: Water rendering modes (translucent, framebuffer reflection, shader-based, 3D mesh).
- **SEA_PATCH_VERTEX (Struct)**: Vertex structure for D3D water rendering.
- **WaterMeshData (Struct)**: Stores height/velocity data for 3D water mesh.
- **Setting (Struct)**: Time-of-day specific water/sky textures and parameters.

## Key Functions
### `renderWater()`
- Purpose: Draws the water surface (flat rendering).
- Calls: Not inferable from header.

### `updateRenderTargetTextures(CameraClass *cam)`
- Purpose: Renders into reflection textures.
- Calls: Not inferable from header.

### `getWaterHeight(Real x, Real y)`
- Purpose: Returns water height at a world position.
- Calls: Not inferable from header.

### `changeGridHeight(Real x, Real y, Real delta)`
- Purpose: Modifies water grid height with falloff.
- Calls: Not inferable from header.

## Globals
- **TheWaterRenderObj (WaterRenderObjClass*)**: Global water rendering instance.

## Dependencies
- Key includes: `rendobj.h`, `w3d_file.h`, `dx8vertexbuffer.h`, `shader.h`, `vertmaterial.h`, `light.h`
- External symbols: `PolygonTrigger`, `WaterTracksRenderSystem`, `Xfer`, `SceneClass`, `CameraClass`, `TextureClass`, `LightClass`, `VertexMaterialClass`
