# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DMirror.h

## Purpose
Defines a custom render object for drawing mirrors, water, and skies in the W3D engine.

## Responsibilities
- Renders reflected W3D scenes for planar surfaces (e.g., water)
- Handles sky rendering (clouds, sky bodies) for reflections
- Manages water surface rendering with texture scrolling
- Provides time-of-day and cloud layer toggling

## Key Types
- **MirrorRenderObjClass (Class)**: Custom render object for mirror/water/sky rendering
- **skySetting (Struct)**: Contains texture and rendering settings per time of day

## Key Functions
### `MirrorRenderObjClass::Render`
- Purpose: Renders the mirror, water, and sky
- Calls: `renderSky`, `renderWater`, `renderWaterMesh`

### `MirrorRenderObjClass::init`
- Purpose: Allocates W3D resources for mirror rendering
- Calls: Not inferable

### `MirrorRenderObjClass::renderSky`
- Purpose: Draws the sky layer (clouds, stars, etc.)
- Calls: `renderSkyBody`

### `MirrorRenderObjClass::renderWater`
- Purpose: Renders the water surface
- Calls: `renderWaterMesh`

## Globals
- **m_tod (TimeOfDay)**: Static time-of-day setting for reflected cloud layer

## Dependencies
- `rendobj.h`, `w3d_file.h`, `dx8vertexbuffer.h`, `dx8indexbuffer.h`, `shader.h`, `vertmaterial.h`
- `Lib/BaseType.h`, `Common/GameType.h`
- `RenderObjClass`, `SceneClass`, `ShaderClass`, `VertexMaterialClass`, `TextureClass`, `TimeOfDay`
