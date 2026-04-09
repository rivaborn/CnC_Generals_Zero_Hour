# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/castres.h - Enhanced Analysis

## Architectural Role
This file defines the core data structure for collision detection results in the SAGE engine's physics subsystem. It serves as the contract between collision detection algorithms and the systems that consume their results (e.g., movement, AI pathfinding, projectile physics).

## Cross-References
### Incoming
- Physics collision detection modules (e.g., ray/volume casting implementations)
- Movement systems (character/vehicle controllers)
- Projectile/bullet physics
- AI pathfinding (obstacle avoidance)

### Outgoing
- References `Vector3` for spatial calculations
- Relies on `W3D_SURFACE_TYPES` (defined elsewhere) for material properties

## Design Patterns
- **Data Transfer Object (DTO)**: Pure data structure with no behavior (except Reset), designed for cross-subsystem communication
- **Option Pattern**: `ComputeContactPoint` flag enables/disables expensive contact point calculation
- **Immutable Defaults**: Reset() provides a clean slate for reuse (likely in object pooling)

*Not inferable*: No clear use of Factory, Observer, or Strategy patterns in this header alone.
