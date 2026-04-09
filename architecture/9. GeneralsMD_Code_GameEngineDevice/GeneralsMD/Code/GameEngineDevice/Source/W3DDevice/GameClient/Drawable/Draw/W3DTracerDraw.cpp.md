# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DTracerDraw.cpp

## Purpose
Handles rendering of tracer effects (e.g., bullet trails) in the game world.

## Responsibilities
- Manages tracer visual properties (color, length, width, opacity)
- Updates tracer position based on movement speed
- Handles tracer creation, transformation, and cleanup
- Supports serialization and CRC for save/load functionality

## Key Types
- **W3DTracerDraw (Class)**: Manages tracer rendering and behavior
- **Line3DClass (External)**: Underlying 3D line renderer used for tracers

## Key Functions
### W3DTracerDraw()
- Purpose: Constructor initializing tracer parameters
- Calls: None

### setTracerParms()
- Purpose: Updates tracer visual and movement parameters
- Calls: `m_theTracer->Reset()`, `m_theTracer->Re_Color()`, `m_theTracer->Set_Opacity()`, `m_theTracer->Set_Transform()`

### doDrawModule()
- Purpose: Renders tracer and updates its position/opacity
- Calls: `NEW Line3DClass()`, `W3DDisplay::m_3DScene->Add_Render_Object()`, `m_theTracer->Set_Transform()`, `m_theTracer->Set_Opacity()`

### reactToTransformChange()
- Purpose: Syncs tracer transform with parent drawable
- Calls: `m_theTracer->Set_Transform()`

## Globals
- **TheGameLogic (External)**: Accesses current frame for expiration calculations

## Dependencies
- `Common/Thing.h`, `Common/ThingTemplate.h`, `Common/Xfer.h`
- `GameClient/Drawable.h`, `GameClient/GameClient.h`
- `GameLogic/GameLogic.h`
- `W3D
