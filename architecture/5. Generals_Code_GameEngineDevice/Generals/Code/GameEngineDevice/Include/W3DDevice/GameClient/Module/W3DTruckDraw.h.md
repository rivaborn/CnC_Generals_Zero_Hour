# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DTruckDraw.h

## Purpose
Defines classes for rendering truck-like vehicles in the game, including wheel rotation, particle effects, and segmented body parts.

## Responsibilities
- Manage truck-specific rendering (wheels, cab, trailer)
- Handle particle effects (dust, dirt, powerslide)
- Control audio events for truck sounds
- Update bone animations for wheels and segmented parts

## Key Types
- **W3DTruckDrawModuleData (Class)**: Stores configuration data for truck rendering (effect names, bone names, rotation factors).
- **W3DTruckDraw (Class)**: Main truck rendering module handling drawing, effects, and bone updates.
- **W3DTruckDrawMagicEnum (Enum)**: Not inferable (likely internal macro enum).
- **W3DTruckDraw_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum).

## Key Functions
### W3DTruckDraw::doDrawModule
- Purpose: Renders the truck with transformations.
- Calls: Not inferable (implementation in .cpp).

### W3DTruckDraw::createEmitters
- Purpose: Initializes particle effects for the truck.
- Calls: Not inferable.

### W3DTruckDraw::enableEmitters
- Purpose: Toggles particle effects on/off.
- Calls: Not inferable.

### W3DTruckDraw::updateBones
- Purpose: Updates wheel and segmented body bone rotations.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `Common/DrawModule.h`
- `Common/AudioEventRTS.h`
- `GameClient/ParticleSys.h`
- `W3DDevice/GameClient/Module/W3DModelDraw.h`
- `WW3D2/HAnim.h`
