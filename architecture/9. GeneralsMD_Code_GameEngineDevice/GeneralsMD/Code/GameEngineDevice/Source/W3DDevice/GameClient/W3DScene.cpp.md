# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DScene.cpp

## Purpose
Manages 3D scene rendering for the game, handling objects, lights, occlusion, and special effects.

## Responsibilities
- Manages render objects, lights, and dynamic lights
- Handles visibility checks and occlusion detection
- Processes special rendering effects (shroud, heat vision, etc.)
- Manages translucent and occluded object rendering
- Provides ray casting for collision detection

## Key Types
- `RTS3DScene` (Class): Main scene manager for 3D rendering
- `RTS2DScene` (Class): Scene manager for 2D rendering
- `RTS3DInterfaceScene` (Class): Scene manager for 3D interface elements
- `PlayerColorShader` (ShaderClass): Shader for player-colored rendering

## Key Functions
### `DoTrees`
- Purpose: Renders tree objects in the scene
- Calls: Not inferable

### `DoShadows`
- Purpose: Renders shadows in the scene
- Calls: Not inferable

### `DoParticles`
- Purpose: Renders particle effects in the scene
- Calls: Not inferable

### `playerIndexToColorIndex`
- Purpose: Converts player index to color index for rendering
- Calls: Not inferable

### `renderStenciledPlayerColor`
- Purpose: Renders objects with stenciled player colors
- Calls: Not inferable

### `flagOccludedObjects`
- Purpose: Identifies objects occluded by others using ray casting
- Calls: `Cast_Ray`, `Cull_Sphere`

### `castRay`
- Purpose: Performs ray intersection tests against scene objects
- Calls: `Cast_Ray` on render objects

### `flushTranslucentObjects`
- Purpose: Renders translucent objects after main scene rendering
- Calls: `renderOneObject`, `Flush`, `Render_And_Clear_Static_Sort_Lists`

## Globals
- `PlayerColorShader` (ShaderClass): Shader for player-colored rendering

## Dependencies
- Key includes: `W3DScene.h`, `WW3D2/camera.h`, `WW3D2/dx8renderer.h`, `GameClient/Drawable.h`
- External symbols: `DoTrees`, `DoShadows`, `DoParticles` (external functions)
