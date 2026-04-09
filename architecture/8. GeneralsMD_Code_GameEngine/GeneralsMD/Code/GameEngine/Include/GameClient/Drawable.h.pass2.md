# GeneralsMD/Code/GameEngine/Include/GameClient/Drawable.h - Enhanced Analysis

## Architectural Role
Core abstraction for all renderable game entities in the SAGE engine. Acts as the bridge between game logic (Thing/Object) and rendering (W3D), managing visual state, animations, and UI overlays. Critical for both client-side rendering and network synchronization.

## Cross-References
### Incoming
- GameClient/Thing.cpp (calls draw/updateDrawable)
- GameClient/Object.cpp (uses setModelConditionState)
- GameClient/ClientUpdateModule.cpp (accesses m_modules)
- GameClient/View.cpp (calls draw during rendering passes)

### Outgoing
- Common/AudioEventRTS.h (uses DynamicAudioEventRTS)
- GameClient/DrawModule.h (manages module rendering)
- WWMath/Matrix3D.h (transformations)
- GameClient/Color.h (tinting/opacity)

## Design Patterns
- **Composite**: Manages multiple DrawModules via m_modules array
- **State**: ModelConditionFlags track visual state transitions
- **Observer**: Icon system dynamically updates UI elements per-frame

*Not inferable*: Exact factory pattern usage for module creation.
