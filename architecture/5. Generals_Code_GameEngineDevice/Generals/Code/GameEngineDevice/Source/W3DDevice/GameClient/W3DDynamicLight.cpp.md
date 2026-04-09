# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DDynamicLight.cpp

## Purpose
Handles dynamic lighting effects with fade-in/fade-out behavior in the W3D rendering system.

## Responsibilities
- Manages dynamic light state (enabled/disabled)
- Controls light intensity and range over time
- Handles fade-in and fade-out transitions
- Updates light properties per frame

## Key Types
- W3DDynamicLight (Class): dynamic light with fade behavior
- LightClass (Enum): light type classification

## Key Functions
### W3DDynamicLight::On_Frame_Update
- Purpose: Updates light properties based on current fade state
- Calls: None

### W3DDynamicLight::setFrameFade
- Purpose: Configures fade-in and fade-out timing
- Calls: None

## Globals
None

## Dependencies
- W3DDynamicLight.h (header)
- LightClass (from W3DDevice)
- Standard types: UnsignedInt, Real
