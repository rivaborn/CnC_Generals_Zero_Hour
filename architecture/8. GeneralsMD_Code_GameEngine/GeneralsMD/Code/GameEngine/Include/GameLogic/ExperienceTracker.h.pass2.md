# GeneralsMD/Code/GameEngine/Include/GameLogic/ExperienceTracker.h - Enhanced Analysis

## Architectural Role
This header defines the core experience management system for units, bridging game logic (veterancy progression) with networking (via `Snapshot`) and memory management (via `MemoryPoolObject`). It enables shared experience delegation (sinks) and scales experience gain dynamically.

## Cross-References
### Incoming
- **Unit classes** (e.g., `Infantry`, `Vehicle`) instantiate `ExperienceTracker` for veterancy tracking.
- **Combat systems** call `addExperiencePoints`/`gainExpForLevel` when units kill enemies.
- **Save/load** subsystems invoke `crc`/`xfer` for serialization.

### Outgoing
- **`Object` hierarchy** for parent reference and experience sink delegation.
- **`Snapshot` interface** for network synchronization.
- **`Xfer` class** for serialization operations.

## Design Patterns
- **Observer (loose coupling)**: Experience sinks allow indirect experience sharing without tight dependencies.
- **Strategy (implicit)**: Experience scaling (`m_experienceScalar`) modularizes bonus logic.
- **Composite (via `Object`)**: Embedded in unit hierarchy, enabling recursive experience delegation.
