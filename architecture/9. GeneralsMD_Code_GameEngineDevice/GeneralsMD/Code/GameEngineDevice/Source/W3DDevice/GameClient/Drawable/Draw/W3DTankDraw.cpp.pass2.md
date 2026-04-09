# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DTankDraw.cpp - Enhanced Analysis

## Architectural Role
This file implements the visual representation of turreted tanks in the SAGE engine, bridging the gap between game logic (physics, AI) and rendering. It extends the base `W3DModelDraw` class to handle tank-specific visual effects like tread animation and debris, demonstrating how the engine separates rendering concerns from game state.

## Cross-References
### Incoming
- Called by the game's draw system when rendering tank units
- Used by the module initialization system during thing creation

### Outgoing
- Calls into `W3DModelDraw` base class for common rendering functionality
- Interacts with `TheParticleSystemManager` for debris effects
- Queries `PhysicsBehavior` and `AIUpdateInterface` for movement state
- Uses `TheTacticalView` and `TheScriptEngine` for game state checks

## Design Patterns
- **Template Method**: Extends `W3DModelDraw::doDrawModule` with tank-specific behavior
- **Observer**: Reacts to physics/AI state changes to drive visual updates
- **Resource Pooling**: Manages particle system emitters with create/destroy lifecycle

*Not inferable*: Exact relationship with modding system or serialization hooks.
