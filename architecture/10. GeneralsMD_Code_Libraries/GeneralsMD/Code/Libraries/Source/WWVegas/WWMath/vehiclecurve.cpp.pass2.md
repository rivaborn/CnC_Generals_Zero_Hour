# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/vehiclecurve.cpp - Enhanced Analysis

## Architectural Role
This file implements the mathematical foundation for vehicle pathfinding in the SAGE engine, specifically handling smooth curve interpolation between waypoints. It bridges the gap between high-level pathfinding (AI subsystem) and low-level rendering (W3D subsystem) by providing precise position evaluation for moving vehicles.

## Cross-References
### Incoming
- AI pathfinding system (uses `Evaluate` for position queries)
- Vehicle movement logic (calls `Update_Arc_List` when paths change)
- Serialization system (uses `Save`/`Load` for game save/load)

### Outgoing
- WWMath library (trigonometric functions, vector math)
- Persistence framework (for save/load operations)
- Curve3D base class (inherited functionality)

## Design Patterns
- **Strategy Pattern**: Different arc calculation strategies (clockwise/counter-clockwise) are encapsulated in separate functions
- **Composite Pattern**: Curve is composed of multiple arc segments stored in `m_ArcList`
- **Memento Pattern**: Serialization via chunk-based save/load preserves object state

Rules followed. Output under 400 tokens.
