# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DParticleSys.cpp

## Purpose
Implements the W3D particle system manager for rendering particles in the game.

## Responsibilities
- Manages particle system rendering via `PointGroupClass` and `StreakLineClass`
- Handles particle culling based on frustum and terrain bounds
- Updates particle buffers (position, color, size, angle)
- Renders particles with different shader types (additive, alpha, etc.)

## Key Types
- `W3DParticleSystemManager` (Class): Manages particle system rendering and buffers
- `PointGroupClass` (Class): Renders point-based particles
- `StreakLineClass` (Class): Renders streak effects for particles
- `ShareBufferClass` (Template): Manages shared buffers for particle data

## Key Functions
### `queueParticleRender`
- Purpose: Flags the particle system as ready to render.
- Calls: None

### `DoParticles`
- Purpose: Entry point for rendering all particles (called by `WW3D::Flush()`).
- Calls: `TheParticleSystemManager->doParticles(rinfo)`

### `doParticles`
- Purpose: Renders all active particle systems.
- Calls:
  - `rinfo.Camera.Get_Frustum()`
  - `TheTerrainRenderObject->getMaximumVisibleBox()`
  - `W3DDisplay::m_assetManager->Get_Texture()`
  - `m_pointGroup->Render()` / `m_pointGroup->RenderVolumeParticle()`
  - `m_streakLine->Render()`

## Globals
- `TheParticleSystemManager` (W3DParticleSystemManager*): Singleton instance of the particle system manager

## Dependencies
- `GameClient/Color.h`, `W3DDevice/GameClient/W3DParticleSys.h`, `W3DDevice/GameClient/W3DAssetManager.h`, `W3DDevice/GameClient/W3DDisplay.h`, `W3DDevice/GameClient/heightmap.h`, `WW3D2/Camera.h`
- `Common/QuickTrig.h`
- `PointGroupClass`, `StreakLineClass`, `ShareBufferClass`, `ParticleSystem`, `Particle`, `RenderInfoClass`, `FrustumClass`, `AABoxClass`, `TextureClass`, `ShaderClass`
