# Generals/Code/Libraries/Source/WWVegas/WW3D2/intersec.h - Enhanced Analysis

## Architectural Role
This file is the core of the SAGE engine's 3D intersection system, bridging rendering (W3D) and game logic. It provides the mathematical foundation for ray casting, collision detection, and screen-to-world coordinate conversion, critical for both UI interaction (e.g., unit selection) and game mechanics (e.g., projectile impacts).

## Cross-References
### Incoming
- **Rendering System**: Uses `RenderObjClass` for hierarchy traversal and polygon intersection.
- **Layer System**: Depends on `LayerClass` for screen-space to world-space ray conversion.
- **Game Logic**: Called by UI and input systems for click detection, and by projectile/AI systems for collision tests.

### Outgoing
- **Math Library**: Relies on `Vector3`, `Matrix3D` for geometric operations.
- **W3D Rendering**: Interacts with `RenderObjClass` for mesh and hierarchy data.
- **Scene Graph**: Uses `LayerClass` for depth management in screen-space intersections.

## Design Patterns
- **Strategy Pattern**: Intersection methods (e.g., `Intersect_Plane`, `Intersect_Polygon`) are modular strategies selectable via `ConvexTest` flag.
- **Flyweight Pattern**: Static `_RayLocation`, `_RayDirection` reduce memory overhead for temporary intersection tests.
- **Visitor Pattern**: `Intersect_RenderObject` traverses object hierarchies, applying intersection tests to each node.
