# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DPoliceCarDraw.cpp

## Purpose
Handles rendering logic for the police car vehicle in the game.

## Responsibilities
- Manages dynamic lighting for the police car's searchlight
- Controls animation frames for the police car model
- Handles color transitions for the searchlight effect
- Manages light lifecycle (creation/destruction)
- Implements serialization (Xfer) and CRC for network sync

## Key Types
- `W3DPoliceCarDraw` (Class): Police car rendering component
- `W3DDynamicLight` (Class): Dynamic light used for searchlight effect

## Key Functions
### `createDynamicLight`
- Purpose: Creates and configures a dynamic light for the searchlight
- Calls: `W3DDisplay::m_3DScene->getADynamicLight()`

### `doDrawModule`
- Purpose: Renders the police car with animated searchlight effect
- Calls: `getRenderObject()`, `getDrawable()->getPosition()`, `W3DTruckDraw::doDrawModule()`

### `xfer`
- Purpose: Serializes police car draw state for network sync
- Calls: `W3DTruckDraw::xfer()`

## Globals
- None

## Dependencies
- `W3DTruckDraw` (base class)
- `W3DDisplay`, `W3DScene`, `HAnimClass`, `RenderObjClass`
- `Xfer`, `Thing`, `Vector3`, `Matrix3D`
