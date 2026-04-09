# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/sampler.h - Enhanced Analysis

## Architectural Role
This file defines the core sampling infrastructure used for procedural generation and statistical distribution in the SAGE engine. It provides algorithms for generating points in multidimensional space, likely used in rendering (e.g., lighting, shadow maps), AI pathfinding, and particle effects.

## Cross-References
### Incoming
- **Rendering Subsystem**: Uses samplers for anti-aliasing, texture filtering, or lightmap generation.
- **AI Pathfinding**: Likely employs stratified sampling for waypoint distribution.
- **Particle Effects**: Uses random/grid sampling for emitter placement.

### Outgoing
- **Random4Class**: Dependency for random number generation in `RandomSamplingClass`.
- **W3D Rendering**: Indirectly called for texture sampling or shader inputs.

## Design Patterns
- **Strategy Pattern**: Abstract `SamplingClass` with concrete implementations allows runtime selection of sampling algorithms.
- **State Pattern**: Internal indices (`index`) track sampling state, enabling sequence continuity.
- **Template Method**: `Sample()` is the primary interface, with subclasses implementing specific logic.
