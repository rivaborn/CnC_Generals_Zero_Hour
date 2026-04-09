# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DMirror.h

## Purpose
Defines a custom render object for drawing mirrors, water, and skies in the W3D engine.

## Responsibilities
- Renders reflected W3D scenes for rectangular planar surfaces
- Handles water and sky rendering with time-of-day effects
- Manages texture scrolling and cloud layer toggling
- Provides bounding volume queries for collision detection

## Key Types
- **MirrorRenderObjClass (Class)**: Custom render object for mirror/water/sky rendering
- **skySetting (Struct)**: Contains texture and color settings per time of day

## Key Functions
### MirrorRenderObjClass::Render
- Purpose: Renders the mirror, water, and sky
- Calls: renderSky, renderWater, renderWaterMesh

### MirrorRenderObjClass::init
- Purpose: Allocates W3D resources for mirror rendering
- Calls: Not inferable

### MirrorRenderObjClass::setTimeOfDay
- Purpose: Updates sky/water settings based on time of day
- Calls: Not inferable

### MirrorRenderObjClass::toggleCloudLayer
- Purpose: Enables/disables the cloud layer
- Calls: Not inferable

## Globals
- **m_tod (TimeOfDay)**: Static time of day setting for reflected cloud layer

## Dependencies
- `rendobj.h`, `w3d_file.h`, `dx8vertexbuffer.h`, `dx8indexbuffer.h`, `shader.h`, `vertmaterial.h`
- `Lib/BaseType.h`, `Common/GameType.h`
- `RenderObjClass`, `SceneClass`, `ShaderClass`, `VertexMaterialClass`, `TextureClass`, `TimeOfDay`
