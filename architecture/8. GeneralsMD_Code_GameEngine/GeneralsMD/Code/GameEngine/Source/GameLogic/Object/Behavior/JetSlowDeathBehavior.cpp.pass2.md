# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/JetSlowDeathBehavior.cpp - Enhanced Analysis

## Architectural Role
This file implements the specialized death behavior for jet units, extending the base `SlowDeathBehavior` to handle multi-stage destruction sequences with timed effects, physics manipulation, and ground impact detection. It bridges the game logic layer with rendering (FX) and audio systems.

## Cross-References
### Incoming
- Called by `Object` destruction logic when a jet unit dies
- Referenced in `ThingTemplate` parsing for behavior module initialization

### Outgoing
- Uses `FXList::doFXObj` for visual effects
- Uses `ObjectCreationList::create` for spawning debris/objects
- Interacts with `PhysicsBehavior` for in-flight physics
- Uses `TheAudio` for death sound management
- Queries `TheTerrainLogic` for ground collision detection

## Design Patterns
- **Template Method**: Extends `SlowDeathBehavior` with jet-specific death stages
- **State Machine**: Manages death sequence through timed frame counters
- **Dependency Injection**: Receives module data via constructor for configuration

*Not inferable*: Exact timing/physics calculations not fully visible in truncated content.
