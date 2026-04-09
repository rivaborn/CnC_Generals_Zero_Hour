# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/vector2i.h - Enhanced Analysis

## Architectural Role
This file defines a fundamental 2D integer vector class used throughout the engine for coordinate storage and manipulation. It serves as a building block for spatial operations in rendering, pathfinding, and game logic subsystems.

## Cross-References
### Incoming
- **WWMath subsystem**: Used by other math utilities (e.g., vector3i.h, matrix classes)
- **Rendering (W3D)**: Likely used for screen/tile coordinates
- **AI/Pathfinding**: Used for grid-based position calculations
- **Game Logic**: Used for unit positioning and map coordinates

### Outgoing
- **None**: This is a standalone utility class with no external dependencies beyond basic C++ types.

## Design Patterns
- **Value Object**: Immutable-like behavior (no setters except `Set()`), designed for pass-by-value usage
- **Operator Overloading**: Provides natural syntax for comparisons and element access
- **Efficient Swap**: Uses XOR trick for branchless swapping (performance optimization for hot paths)
