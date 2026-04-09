# Generals/Code/GameEngine/Source/GameLogic/Object/Behavior/AutoHealBehavior.cpp - Enhanced Analysis

## Architectural Role
The `AutoHealBehavior` class is integral to the game logic, specifically managing the auto-healing functionality for game objects. It interacts with various subsystems such as particle systems, animation, and partition management to provide visual effects and determine which objects are eligible for healing.

## Cross-References
### Incoming
- **GameLogic/Object.h**: Calls `AutoHealBehavior` constructor and destructor.
- **GameLogic/PartitionManager.h**: Uses `iterateObjectsInRange` to find nearby objects for healing.
- **GameClient/ParticleSys.h**: Manages particle systems for visual effects.
- **GameClient/Anim2D.h**: Adds world animations when healing occurs.

### Outgoing
- **ParticleSystemManager**: Creates and destroys particle systems.
- **GameLogic**: Accesses game logic state, such as frame numbers and player control.
- **PartitionManager**: Iterates over objects within a specified radius.
- **Anim2DCollection**: Finds animation templates for visual effects.

## Design Patterns
- **Observer Pattern**: The `onDamage` method acts as an observer to damage events, resetting the healing process when necessary.
- **Strategy Pattern**: Different healing strategies are applied based on configuration (`m_radius == 0.0f` for self-healing vs. healing nearby allies).
- **Singleton Pattern**: Uses global instances like `TheParticleSystemManager`, `TheGameLogic`, and `TheAnim2DCollection`.
