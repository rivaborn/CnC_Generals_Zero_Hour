# GeneralsMD/Code/GameEngine/Source/Common/System/Trig.cpp - Enhanced Analysis

## Architectural Role
This file provides optimized trigonometric functions used throughout the engine for vector math, rotation calculations, and physics. The lookup-table approach ensures consistent performance across different hardware, critical for real-time game calculations.

## Cross-References
### Incoming
- **Game Logic**: Unit movement, projectile trajectories
- **W3D Rendering**: Model transformations, camera rotations
- **AI**: Pathfinding, unit orientation
- **Physics**: Collision detection, force calculations

### Outgoing
- **None**: Pure utility library with no external dependencies

## Design Patterns
- **Lookup Table Pattern**: Precomputed values for O(1) trigonometric operations
- **Strategy Pattern**: Runtime switch between standard lib and lookup tables via `DEFAULT_TRIG`
- **Singleton-like Initialization**: Global trig tables initialized once via `TrigInit` class

Key insight: The lookup tables were hardware-specific (generated on a PIII), suggesting performance tuning for the target platform. The `DEFAULT_TRIG` switch allows fallback to standard lib for debugging or precision-critical cases.
