# Generals/Code/Libraries/Source/WWVegas/WWMath/vehiclecurve.h - Enhanced Analysis

## Architectural Role
This file defines the `VehicleCurveClass`, which is part of the pathfinding and movement system for vehicle units. It extends the base `Curve3DClass` to handle vehicle-specific path calculations, including turn arcs and sharpness metrics, which are critical for realistic vehicle movement in the game world.

## Cross-References
### Incoming
- **Pathfinding System**: Likely called by the AI or movement controller to generate smooth paths for vehicles.
- **Unit Movement Logic**: Used by vehicle units to determine their next position based on time and curve evaluation.
- **Serialization System**: Called during game save/load to persist vehicle path data.

### Outgoing
- **Curve3DClass**: Inherits and extends functionality for 3D curve evaluation.
- **PersistFactoryClass**: Used for save/load operations.
- **ChunkSaveClass/ChunkLoadClass**: Handles binary serialization of curve data.

## Design Patterns
- **Template Method Pattern**: The `Evaluate` method is overridden to provide vehicle-specific curve evaluation while reusing base class logic.
- **Dirty Flag Pattern**: Uses `m_IsDirty` to defer expensive recalculations (e.g., `Update_Arc_List`) until necessary.
- **Composite Pattern**: The `ARC_LIST` (dynamic vector of `ArcInfoStruct`) aggregates arc segments to form the overall vehicle path.

*Not inferable*: Exact usage of `Sharpness` metric or how `Update_Arc_List` computes arcs.
