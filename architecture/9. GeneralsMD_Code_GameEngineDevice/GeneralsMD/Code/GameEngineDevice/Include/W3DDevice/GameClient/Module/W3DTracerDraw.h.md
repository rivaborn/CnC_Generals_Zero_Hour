# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DTracerDraw.h

## Purpose
Defines the W3DTracerDraw class, a DrawModule for rendering tracer effects in the W3D scene.

## Responsibilities
- Rendering tracer effects (e.g., bullet trails, missile paths)
- Managing tracer parameters (speed, length, width, color, opacity)
- Implementing TracerDrawInterface for external control
- Reacting to transform changes (position/rotation updates)

## Key Types
- **W3DTracerDraw (Class)**: DrawModule for rendering tracers in W3D.
- **W3DTracerDrawMagicEnum (Enum)**: Not inferable (likely internal macro enum).
- **W3DTracerDraw_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum).

## Key Functions
### W3DTracerDraw::doDrawModule
- Purpose: Renders the tracer effect.
- Calls: Not inferable (implementation in .cpp).

### W3DTracerDraw::reactToTransformChange
- Purpose: Updates tracer position/rotation when parent object moves.
- Calls: Not inferable.

### W3DTracerDraw::setTracerParms
- Purpose: Configures tracer visual properties (speed, length, width, color, opacity).
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `Common/DrawModule.h` (base class)
- `WW3D2/Line3D.h` (tracer rendering)
- `TracerDrawInterface` (external interface, not defined here)
