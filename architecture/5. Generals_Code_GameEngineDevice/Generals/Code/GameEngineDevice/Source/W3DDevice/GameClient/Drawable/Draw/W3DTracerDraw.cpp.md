# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DTracerDraw.cpp

## Purpose
Handles rendering of tracer effects (e.g., bullet trails) in the game world.

## Responsibilities
- Manages creation and rendering of tracer objects
- Handles tracer movement and opacity changes over time
- Updates tracer position based on thing's transform
- Cleans up tracer resources when destroyed

## Key Types
- `W3DTracerDraw` (Class): Draw module for tracer effects
- `Line3DClass` (External): Render object for the tracer line

## Key Functions
### `W3DTracerDraw::W3DTracerDraw`
- Purpose: Constructor initializes tracer parameters
- Calls: None

### `W3DTracerDraw::setTracerParms`
- Purpose: Updates tracer visual properties
- Calls: `m_theTracer->Reset`, `m_theTracer->Re_Color`, `m_theTracer->Set_Opacity`, `m_theTracer->Set_Transform`

### `W3DTracerDraw::doDrawModule`
- Purpose: Creates and renders the tracer each frame
- Calls: `NEW Line3DClass`, `W3DDisplay::m_3DScene->Add_Render_Object`, `m_theTracer->Set_Transform`, `m_theTracer->Set_Opacity`

### `W3DTracerDraw::reactToTransformChange`
- Purpose: Updates tracer transform when parent thing moves
- Calls: `m_theTracer->Set_Transform`

## Globals
- None

## Dependencies
- `Common/Thing.h`, `Common/ThingTemplate.h`, `Common/Xfer.h`
- `GameClient/Drawable.h`, `GameClient/GameClient.h`
- `GameLogic/GameLogic.h`
- `W3DDevice
