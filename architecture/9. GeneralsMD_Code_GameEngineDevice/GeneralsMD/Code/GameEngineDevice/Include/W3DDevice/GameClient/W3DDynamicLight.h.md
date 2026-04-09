# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DDynamicLight.h

## Purpose
Manages dynamic lighting effects for terrain rendering in the W3D engine.

## Responsibilities
- Controls light enable/disable states and fading effects
- Tracks light influence boundaries for culling
- Manages decay and intensity transitions over frames
- Provides access to light properties for terrain rendering

## Key Types
- **W3DDynamicLight (Class)**: Dynamic light manager for terrain
- **HeightMapRenderObjClass (Class)**: External terrain renderer (friend class)

## Key Functions
### W3DDynamicLight()
- Purpose: Constructor initializes dynamic light state
- Calls: None

### On_Frame_Update()
- Purpose: Updates light properties each frame (decay, fading)
- Calls: None

### setFrameFade()
- Purpose: Configures light fade-in/out timing
- Calls: None

### cull()
- Purpose: Checks if terrain vertex is outside light influence
- Calls: None

## Globals
- None

## Dependencies
- `LightClass` (base class)
- `Vector3` (for color values)
- `HeightMapRenderObjClass` (friend class)
