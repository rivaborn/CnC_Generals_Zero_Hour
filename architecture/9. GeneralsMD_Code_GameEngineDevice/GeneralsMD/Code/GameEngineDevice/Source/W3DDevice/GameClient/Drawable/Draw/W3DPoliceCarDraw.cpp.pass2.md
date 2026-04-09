# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DPoliceCarDraw.cpp - Enhanced Analysis

## Architectural Role
This file implements the visual behavior of the police car vehicle, extending the base truck rendering class. It handles the searchlight effect through dynamic lighting and animation, demonstrating how specialized vehicle effects are integrated into the SAGE engine's rendering pipeline.

## Cross-References
### Incoming
- `W3DDisplay` (uses `m_3DScene->getADynamicLight()`)
- `W3DTruckDraw` (base class, called in constructor/destructor)
- `HAnimClass` (animation control via `Peek_Animation()`)
- `Xfer` (serialization system)

### Outgoing
- `W3DScene` (light management)
- `Drawable` (position access)
- `RenderObjClass` (model rendering)

## Design Patterns
- **Template Method**: Extends `W3DTruckDraw::doDrawModule()` while adding police-car-specific behavior
- **Object Pooling**: Reuses dynamic lights from the scene (via `getADynamicLight()`)
- **State Machine**: Frame-based color transitions simulate searchlight cycling (not inferable as formal pattern)
