# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DPoliceCarDraw.h

## Purpose
Defines the `W3DPoliceCarDraw` class, a specialized draw module for police cars in the game.

## Responsibilities
- Extends `W3DTruckDraw` to handle police car-specific rendering
- Manages dynamic lighting for police car search lights
- Implements frame-based animation for the police car model

## Key Types
- **W3DPoliceCarDraw (Class)**: Police car rendering module
- **W3DPoliceCarDrawMagicEnum (Enum)**: Not inferable
- **W3DPoliceCarDraw_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### W3DPoliceCarDraw::doDrawModule
- Purpose: Renders the police car model with current transformation
- Calls: Not inferable

### W3DPoliceCarDraw::createDynamicLight
- Purpose: Creates a dynamic light for the police car's search light
- Calls: Not inferable

## Globals
- **m_light (W3DDynamicLight*)**: Stores the search light dynamic light
- **m_curFrame (Real)**: Tracks current animation frame

## Dependencies
- `Common/DrawModule.h`
- `W3DDevice/GameClient/Module/W3DTruckDraw.h`
- `W3DDevice/GameClient/W3DDynamicLight.h`
- `WW3D2/Line3D.h`
