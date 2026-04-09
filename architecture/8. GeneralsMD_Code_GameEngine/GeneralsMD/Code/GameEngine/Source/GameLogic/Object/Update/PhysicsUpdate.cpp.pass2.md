# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/PhysicsUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the core physics simulation system for the SAGE engine, handling rigid-body dynamics, collision response, and force application. It bridges the game logic layer with the rendering system by managing object transformations and state updates.

## Cross-References
### Incoming
- **AIUpdate.h**: Uses `hasLocomotorForSurface` for terrain compatibility checks
- **BodyModule.h**: Likely called by body-related systems for physics updates
- **ContainModule.h**: May be invoked during containment physics interactions
- **CrushDie.h**: References `CrushEnum` for vehicle crushing mechanics
- **Object.h**: Core object system calls physics updates
- **TerrainLogic.h**: Queries terrain state for collision responses

### Outgoing
- **Common/Xfer.h**: Uses serialization for networking
- **GameLogic/GameLogic.h**: Accesses global game state
- **GameLogic/Weapon.h**: Triggers weapon effects on collisions
- **ScriptEngine.h**: May be called by scripted physics events

## Design Patterns
- **Module Pattern**: PhysicsBehavior inherits from UpdateModule, following the engine's modular architecture
- **Data-Driven Design**: Physics parameters (mass, friction) are configurable via INI, enabling modding
- **State Machine**: Uses flags (IS_STUNNED) to manage object states and transitions

*Not inferable*: Exact pattern usage in truncated sections (e.g., force application logic).
