# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DDynamicLight.cpp

## Purpose
Handles dynamic lighting effects with fade-in/fade-out behavior in the W3D rendering system.

## Responsibilities
- Manages dynamic light state (enabled/disabled)
- Handles frame-based intensity and range fading
- Updates light properties per frame
- Supports configurable fade-in and fade-out durations

## Key Types
- `W3DDynamicLight` (Class): Dynamic light with fade behavior
- `LightClass` (Enum): Light type classification

## Key Functions
### `W3DDynamicLight::On_Frame_Update`
- Purpose: Updates light properties based on current fade state
- Calls: None

### `W3DDynamicLight::setFrameFade`
- Purpose: Configures fade-in and fade-out durations
- Calls: None

## Globals
None

## Dependencies
- `W3DDynamicLight.h` (header)
- `LightClass` (from external header)
- Standard types: `UnsignedInt`, `Real`
