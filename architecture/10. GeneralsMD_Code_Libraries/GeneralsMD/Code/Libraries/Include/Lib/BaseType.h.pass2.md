# GeneralsMD/Code/Libraries/Include/Lib/BaseType.h - Enhanced Analysis

## Architectural Role
This header serves as the foundational type system for the entire engine, providing cross-cutting data structures and utilities used by rendering (W3D), physics, AI pathfinding, and game logic subsystems. Its coordinate and region types form the spatial backbone for collision detection and visibility systems.

## Cross-References
### Incoming
- Rendering pipeline (W3D) for coordinate transformations
- AI pathfinding for region containment checks
- Physics system for vector operations
- UI system for color conversions

### Outgoing
- Directly uses `<math.h>` for trigonometric functions
- References "Lib/Trig.h" for angle utilities
- Uses inline assembly for performance-critical conversions

## Design Patterns
- **Primitive Objection Pattern**: Wraps fundamental types (Real, Int) to enforce type safety across subsystems
- **Structural Composition**: Combines coordinate/region types to build spatial hierarchies
- **Template Method**: Generic `clamp` and `sqr` functions work across numeric types

*Not inferable*: No clear use of Factory, Observer, or Visitor patterns in this header.
