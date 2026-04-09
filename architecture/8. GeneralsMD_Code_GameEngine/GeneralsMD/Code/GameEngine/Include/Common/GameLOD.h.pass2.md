# GeneralsMD/Code/GameEngine/Include/Common/GameLOD.h - Enhanced Analysis

## Architectural Role
This file defines the core LOD (Level of Detail) management system, bridging hardware detection, rendering optimization, and performance scaling. It serves as the central authority for dynamic and static LOD decisions, influencing particle systems, debris rendering, and texture quality across the engine.

## Cross-References
### Incoming
- **Rendering Subsystem**: Uses `isParticleSkipped`/`isDebrisSkipped` for performance-based culling
- **Particle System**: Queries `getMinDynamicParticlePriority` for priority-based rendering
- **UI/Options Menu**: Calls `getStaticGameLODLevelName`/`getDynamicGameLODLevelName` for display
- **Game Initialization**: Invokes `findStaticLODLevel` during startup hardware profiling

### Outgoing
- **Hardware Detection**: Relies on external CPU/GPU detection (not shown in header)
- **INI Configuration**: Uses `FieldParse` table for INI-based LOD presets (likely in `gamelod.cpp`)
- **Texture System**: Adjusts texture reduction via `setCurrentTextureReduction`

## Design Patterns
- **Strategy Pattern**: LOD presets act as interchangeable strategies for different hardware tiers
- **Singleton**: `TheGameLODManager` global instance (implied by extern declaration)
- **Data-Driven Design**: LOD thresholds and presets are configurable via INI/benchmarks

*Not inferable*: Exact particle priority enum definition or benchmark calculation logic.
