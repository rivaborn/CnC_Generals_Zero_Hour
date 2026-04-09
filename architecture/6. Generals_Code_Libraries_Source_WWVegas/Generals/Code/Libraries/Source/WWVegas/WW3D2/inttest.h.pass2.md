# Generals/Code/Libraries/Source/WWVegas/WW3D2/inttest.h - Enhanced Analysis

## Architectural Role
This file defines the core collision detection primitives for the SAGE engine's 3D rendering pipeline, specifically handling intersection tests between geometric primitives. It serves as the foundational layer for spatial queries used in both rendering culling and physics systems.

## Cross-References
### Incoming
- **Rendering System**: Uses these classes for frustum culling and occlusion queries
- **Physics System**: Likely called for collision detection between game entities
- **AI Pathfinding**: May use for navigation mesh queries

### Outgoing
- **Math Library**: Relies heavily on `Vector3`, `Matrix3D`, and `WWMath` for transformations
- **Collision Math**: Delegates actual intersection calculations to `CollisionMath`
- **Geometry Primitives**: Works with `AABoxClass`, `OBBoxClass`, and `TriClass`

## Design Patterns
- **Template Method Pattern**: The base `IntersectionTestClass` defines the interface for culling and intersection tests, with concrete implementations in derived classes
- **Composite Pattern**: The `OBBoxIntersectionTestClass` maintains both an oriented box and its axis-aligned bounding box for hierarchical culling
- **Flyweight Pattern**: The collision type is stored in the base class to avoid duplication across multiple test instances

The non-virtual function design is notable - it's an optimization to avoid virtual call overhead in performance-critical collision detection code.
