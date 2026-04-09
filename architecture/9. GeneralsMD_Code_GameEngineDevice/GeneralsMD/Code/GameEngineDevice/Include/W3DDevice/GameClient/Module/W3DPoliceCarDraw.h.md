# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DPoliceCarDraw.h

## Purpose
Defines the `W3DPoliceCarDraw` class, a specialized draw module for police cars in the game.

## Responsibilities
- Extends `W3DTruckDraw` to handle police car-specific rendering
- Manages dynamic lighting for police car search lights
- Implements frame-based animation for the police car model

## Key Types
- **W3DPoliceCarDraw (Class)**: Police car rendering module.
- **W3DPoliceCarDrawMagicEnum (Enum)**: Not inferable.
- **W3DPoliceCarDraw_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable.

## Key Functions
### `W3DPoliceCarDraw(constructor)`
- Purpose: Initializes the police car draw module.
- Calls: Not inferable.

### `doDrawModule(const Matrix3D* transformMtx)`
- Purpose: Renders the police car with transformations.
- Calls: Not inferable.

### `createDynamicLight()`
- Purpose: Creates a dynamic light for the police car's search light.
- Calls: Not inferable.

## Globals
- **m_light (W3DDynamicLight*)**: Stores the dynamic light for the police car.
- **m_curFrame (Real)**: Tracks the current animation frame.

## Dependencies
- `Common/DrawModule.h`
- `W3DDevice/GameClient/Module/W3DTruckDraw.h`
- `W3DDevice/GameClient/W3DDynamicLight.h`
- `WW3D2/Line3D.h`
