# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DDynamicLight.h

## Purpose
Defines a dynamic light class for the W3D rendering engine, used to generate lighting effects on terrain.

## Responsibilities
- Manages dynamic light properties (range, color, fade effects)
- Tracks light influence boundaries for culling
- Handles frame-based updates for fading and decay
- Provides accessors for light state and parameters

## Key Types
- **W3DDynamicLight (Class)**: Dynamic light entity with fade and decay capabilities
- **HeightMapRenderObjClass (Class)**: Friend class that updates terrain lighting (external)

## Key Functions
### W3DDynamicLight()
- Purpose: Default constructor
- Calls: None

### ~W3DDynamicLight()
- Purpose: Destructor
- Calls: None

### On_Frame_Update()
- Purpose: Updates light properties per frame (handles fading/decay)
- Calls: Not inferable

### setEnabled()
- Purpose: Enables/disables the light and resets fade counters
- Calls: None

### setFrameFade()
- Purpose: Configures fade-in and fade-out timing for the light
- Calls: None

### cull()
- Purpose: Checks if a terrain vertex is outside the light's influence
- Calls: None

## Globals
- None

## Dependencies
- `LightClass` (base class)
- `Vector3` (for color values)
- `WW3D2/Light.h` (header)
- `lib/baseType.h` (header)
