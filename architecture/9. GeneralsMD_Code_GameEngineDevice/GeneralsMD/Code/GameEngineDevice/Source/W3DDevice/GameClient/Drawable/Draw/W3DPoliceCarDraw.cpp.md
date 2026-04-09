# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DPoliceCarDraw.cpp

## Purpose
Handles rendering logic for the police car vehicle in the game.

## Responsibilities
- Manages dynamic lighting for the police car's searchlight
- Controls animation frame progression for the vehicle
- Handles color transitions for the searchlight effect
- Manages light lifecycle (creation/destruction)
- Implements serialization (Xfer) and CRC methods

## Key Types
- `W3DPoliceCarDraw` (Class): Main class handling police car rendering
- `W3DDynamicLight` (Class): Dynamic light used for searchlight effect

## Key Functions
### `createDynamicLight`
- Purpose: Creates and configures a dynamic light for the searchlight
- Calls: `W3DDisplay::m_3DScene->getADynamicLight()`

### `doDrawModule`
- Purpose: Renders the police car with animated searchlight effect
- Calls: `getRenderObject()`, `getDrawable()->getPosition()`, `W3DTruckDraw::doDrawModule()`

### `xfer`
- Purpose: Serializes/deserializes police car draw state
- Calls: `W3DTruckDraw::xfer()`

## Globals
- None

## Dependencies
- `W3DPoliceCarDraw.h`
- `W3DTruckDraw` (base class)
- `W3DDisplay`
- `HAnimClass`
- `Xfer`
- `RandomValue`
