# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DParticleSys.cpp

## Purpose
Implements the W3D particle system manager for rendering particles, smudges, and weather effects in the game.

## Responsibilities
- Manages particle system rendering via `W3DParticleSystemManager`
- Handles particle culling and buffer management
- Renders streaks, point particles, and volume particles
- Integrates with smudge and snow managers for environmental effects
- Provides global particle rendering via `DoParticles()`

## Key Types
- `W3DParticleSystemManager` (Class): Manages particle systems, buffers, and rendering
- `PointGroupClass` (Class): Handles point particle rendering
- `StreakLineClass` (Class): Manages streak line rendering
- `ShareBufferClass` (Template): Buffer management for particle data (position, color, size, angle)

## Key Functions
### `W3DParticleSystemManager::doParticles()`
- Purpose: Renders all active particle systems, smudges, and weather effects
- Calls: `TheSmudgeManager->setSmudgeCountLastFrame()`, `TheTerrainRenderObject->getMaximumVisibleBox()`, `m_pointGroup->Render()`, `m_streakLine->Render()`, `TheSnowManager->render()`, `TheSmudgeManager->render()`

### `DoParticles()`
- Purpose: Global entry point for particle rendering called by `WW3D::Flush()`
- Calls: `TheParticleSystemManager->doParticles()`

## Globals
- `TheParticleSystemManager` (W3DParticleSystemManager*): Global particle system manager instance
- `TheSmudgeManager` (SmudgeManager*): Global smudge manager instance
- `TheSnowManager` (SnowManager*): Global snow manager instance
- `TheTerrainRenderObject` (TerrainRenderObject*): Global terrain render object

## Dependencies
- `common/GlobalData.h`, `GameClient/Color.h`, `W3DDevice/GameClient/W3DParticleSys.h`, `W3DDevice/GameClient/W3DAssetManager.h`, `W3DDevice/GameClient/W3DDisplay.h`, `W3DDevice/GameClient/heightmap.h`, `W3DDevice/GameClient/W3DSmudge.h`, `W3DDevice/GameClient/W3DSnow.h`, `WW3D2/Camera.h`
- `Common/QuickTrig.h` (for trigonometric functions)
- `PointGroupClass`, `StreakLineClass`, `ShareBufferClass`, `ParticleSystem`, `Particle`, `SmudgeSet`, `Smudge`, `TextureClass`, `ShaderClass`, `RenderInfoClass`, `FrustumClass`, `AABoxClass`, `Coord3D`, `RGBColor`, `
