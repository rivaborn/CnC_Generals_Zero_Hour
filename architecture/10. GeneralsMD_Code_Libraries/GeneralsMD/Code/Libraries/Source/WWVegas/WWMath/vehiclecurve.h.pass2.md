# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/vehiclecurve.h - Enhanced Analysis

## Architectural Role
This file defines the `VehicleCurveClass`, which extends the base `Curve3DClass` to model vehicle movement paths with turn arcs. It is part of the WWMath library, providing specialized curve evaluation for vehicle AI pathfinding and movement simulation.

## Cross-References
### Incoming
- **AI Pathfinding**: Likely called by AI movement systems to generate smooth vehicle paths.
- **Unit Movement**: Used by unit controllers to interpolate positions along curves.
- **Serialization**: Called by save/load systems for game state persistence.

### Outgoing
- **Curve3DClass**: Inherits and extends base curve functionality.
- **ChunkSaveClass/ChunkLoadClass**: For serialization support.
- **Vector3**: For geometric calculations and position storage.

## Design Patterns
- **Template Method**: Extends `Curve3DClass` with vehicle-specific behavior while reusing base curve evaluation.
- **Dirty Flag**: Uses `m_IsDirty` to optimize recalculations of arc data only when necessary.
- **Composite**: `ARC_LIST` aggregates arc segments to form the complete vehicle path.

*Not inferable: Specific usage of `m_Sharpness` and `m_SharpnessPos` for collision or pathfinding optimization.*
