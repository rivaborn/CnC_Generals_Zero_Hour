# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/coltest.h - Enhanced Analysis

## Architectural Role
This file defines the core collision detection hierarchy for the SAGE engine's 3D physics system. It bridges between spatial queries (via `Cull`) and precise geometry intersection tests (via `Cast_To_Triangle`), supporting both static and dynamic collision scenarios.

## Cross-References
### Incoming
- Physics system (e.g., `PhysicsClass`) uses these test classes for object movement validation
- Rendering system references `RenderObjClass` for collision object tracking
- AI pathfinding queries collision tests for navigation mesh generation

### Outgoing
- Heavily depends on `CollisionMath` for all actual collision calculations
- Uses `Vector3`/`Matrix3D` for geometric transformations
- Relies on `CastResultStruct` for result propagation

## Design Patterns
- **Composite Pattern**: Hierarchy of collision test classes with shared interface
- **Flyweight Pattern**: Reuses `CastResultStruct` via pointer to avoid copying
- **Template Method Pattern**: Non-virtual `Cull`/`Cast_To_Triangle` with fixed signatures (hinted in comments)
