# Generals/Code/Libraries/Source/WWVegas/WWMath/curve.cpp - Enhanced Analysis

## Architectural Role
This file implements the core animation curve system for the SAGE engine, providing 1D and 3D keyframe-based interpolation used throughout the game for animations, camera paths, and vehicle movement. The persistence support enables saving/loading of curve data, critical for game state serialization.

## Cross-References
### Incoming
- `vehiclecurve.cpp` uses `Evaluate`, `Find_Tangent`, `Find_Tangents`, `Find_Turn_Arc`, and `Get_Angle_Delta` for pathfinding and vehicle movement calculations.

### Outgoing
- Relies on `persistfactory.h` for serialization infrastructure
- Uses `wwmathids.h` for chunk ID definitions
- Depends on `wwhack.h` for assertions and debug utilities

## Design Patterns
- **Factory Pattern**: Uses `SimplePersistFactoryClass` for object creation during deserialization, enabling runtime polymorphism for curve types.
- **Composite Pattern**: Curve classes manage collections of keyframes, treating them as a unified whole for evaluation.
- **Template Method**: `Find_Interval` implementations vary between 1D/3D but follow the same interface, allowing consistent evaluation logic.
