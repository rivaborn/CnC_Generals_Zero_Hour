# Generals/Code/Libraries/Source/WWVegas/WWLib/sampler.cpp - Enhanced Analysis

## Architectural Role
This file implements core sampling algorithms used primarily for rendering effects (e.g., particle systems, lighting) and potentially AI pathfinding or procedural generation. The sampling methods are abstracted to allow different quality/performance tradeoffs across the engine.

## Cross-References
### Incoming
- Likely called by W3D rendering systems (e.g., particle emitters, shader effects)
- May be used by AI for spatial sampling (e.g., patrol points, cover positions)
- Potential usage in terrain generation or procedural content

### Outgoing
- Depends on `Random4Class` for random number generation
- Uses `W3DNEWARRAY` for memory allocation (W3D-specific)
- Relies on `SamplingClass` base class for common interface

## Design Patterns
- **Strategy Pattern**: Different sampling algorithms inherit from `SamplingClass`, allowing runtime selection of sampling method
- **Template Method**: `Sample()` is the template method implemented differently by each subclass
- **Object Pooling**: Memory management via `W3DNEWARRAY` suggests potential pooling for performance-critical sampling

*Not inferable*: Exact usage contexts (e.g., which rendering systems call this) or performance optimizations (e.g., cache locality).
