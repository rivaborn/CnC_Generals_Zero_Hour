# Generals/Code/Libraries/Source/WWVegas/WWLib/sampler.h - Enhanced Analysis

## Architectural Role
This file defines the core sampling infrastructure for procedural generation and spatial distribution in the SAGE engine. It provides algorithms for distributing points in multidimensional space, likely used for particle effects, terrain generation, and AI pathfinding.

## Cross-References
### Incoming
- **Particle Systems**: Uses sampling for emitter placement and particle distribution.
- **Terrain Generation**: Likely used for heightmap or texture sampling.
- **AI Pathfinding**: May be used for waypoint distribution or coverage sampling.

### Outgoing
- **Random4Class**: Depends on this for random number generation in `RandomSamplingClass`.

## Design Patterns
- **Strategy Pattern**: Abstract `SamplingClass` with concrete implementations allows runtime selection of sampling algorithms.
- **State Pattern**: Internal state (e.g., `index` in `QMCSamplingClass`) evolves with each `Sample()` call.
- **Template Method**: `Sample()` is the primary template method, with subclasses implementing the core logic.
