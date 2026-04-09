# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DWater.h

## Purpose
Defines the water rendering system for the SAGE engine, handling water surfaces, reflections, and sky rendering.

## Responsibilities
- Manages water surface rendering (flat, 3D mesh, or shader-based)
- Handles water physics (height changes, velocity, grid deformation)
- Renders sky and cloud layers with time-of-day variations
- Supports water tracks/wakes and river water effects
- Provides collision detection and height queries

## Key Types
- **WaterRenderObjClass (Class)**: Main water rendering object handling reflections, water surfaces, and skies.
- **WaterType (Enum)**: Water rendering modes (translucent, framebuffer reflection, pixel/vertex shader, 3D grid mesh).
- **SEA_PATCH_VERTEX (Struct)**: Vertex structure for D3D water rendering.
- **WaterMeshData (Struct)**: Stores height, velocity, and status for 3D water mesh points.
- **Setting (Struct)**: Time-of-day-specific water/sky textures and rendering parameters.

## Key Functions
### `renderWater()`
- Purpose: Draws the water surface (flat).
- Calls: `drawSea`, `renderWaterMesh`, `drawRiverWater`.

### `updateRenderTargetTextures(CameraClass *cam)`
- Purpose: Renders into required textures (e.g., reflections).
- Calls: `renderMirror`, `getClippedWaterPlane`.

### `changeGridHeight(Real x, Real y, Real delta)`
- Purpose: Adjusts water grid height at a world point with neighbor falloff.
- Calls: None directly (modifies `m_meshData`).

### `worldToGridSpace(Real worldX, Real worldY, Real &gridX, Real &gridY)`
- Purpose: Converts world coordinates to grid-local coordinates.
- Calls: None.

### `init(Real waterLevel, Real dx, Real dy, SceneClass *parentScene, WaterType type)`
- Purpose: Initializes water rendering with dimensions and type.
- Calls: `generateIndexBuffer`, `generateVertexBuffer`, `loadSetting`.

## Globals
- **TheWaterRenderObj (WaterRenderObjClass*)**: Global water rendering object instance.

## Dependencies
- **Key Includes**: `rendobj.h`, `w3d_file.h`, `dx8vertexbuffer.h`, `dx8indexbuffer.h`, `shader.h`, `vertmaterial.h`, `light.h`.
- **External Symbols**: `PolygonTrigger`, `WaterTracksRenderSystem`, `Xfer`, `SceneClass`, `CameraClass`, `TextureClass`, `ShaderClass`, `VertexMaterialClass`, `LightClass`.
