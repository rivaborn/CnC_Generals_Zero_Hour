# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/HelicopterSlowDeathUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the specialized death animation sequence for helicopters, extending the base `SlowDeathBehavior` with helicopter-specific physics (spiral descent, blade detachment) and effects. It bridges the gap between high-level game logic and low-level rendering/physics systems.

## Cross-References
### Incoming
- Called by `SlowDeathBehavior` subclasses when helicopter death is triggered
- Referenced in `ObjectCreationList` for spawning helicopter rubble
- Used by `PhysicsBehavior` for collision detection during death sequence

### Outgoing
- Calls `SlowDeathBehavior` base class methods for common death logic
- Interacts with `TheGameLogic` for object lifecycle management
- Uses `TheTerrainLogic` for ground collision detection
- Leverages `TheAudio` and `TheParticleSystemManager` for effects

## Design Patterns
- **Template Method**: Extends `SlowDeathBehavior` with helicopter-specific implementations while preserving base behavior
- **State Machine**: Manages death sequence phases (spiral, blade fly-off, ground impact, final explosion) via frame counters
- **Dependency Injection**: Receives configuration via `HelicopterSlowDeathBehaviorModuleData` parsed from INI files
