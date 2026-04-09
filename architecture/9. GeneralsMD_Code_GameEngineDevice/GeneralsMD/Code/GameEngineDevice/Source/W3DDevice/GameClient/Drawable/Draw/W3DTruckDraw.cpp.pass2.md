# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DTruckDraw.cpp - Enhanced Analysis

## Architectural Role
This file implements the visual representation layer for truck-like vehicles in the SAGE engine, bridging physics simulation (via `PhysicsBehavior`) and rendering (via `W3DModelDraw`). It handles real-time animation of vehicle components (wheels, cab, trailer) and environmental effects (dust, dirt) based on game state.

## Cross-References
### Incoming
- **Physics System**: `PhysicsBehavior` calls `doDrawModule` to synchronize visual state with simulation
- **AI System**: `AIUpdateInterface` influences wheel rotation via `m_wheelAngle` updates
- **Audio System**: `GameAudio` triggers sound events during powerslides/landings

### Outgoing
- **Rendering Pipeline**: Uses `W3DRenderObject::Control_Bone` for skeletal animation
- **Particle System**: Creates/destroys emitters via `TheParticleSystemManager`
- **Scripting**: Accesses `TheScriptEngine` for template data during initialization

## Design Patterns
- **Component Pattern**: Extends `W3DModelDraw` to encapsulate truck-specific rendering logic
- **Observer Pattern**: Reacts to physics state changes (velocity, acceleration) to update visuals
- **Resource Pooling**: Manages particle emitters with `createEmitters`/`tossEmitters` lifecycle

*Not inferable*: No clear use of Strategy or Factory patterns despite modular effect handling.
