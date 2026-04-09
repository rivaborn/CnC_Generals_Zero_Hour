# Generals/Code/Libraries/Source/WWVegas/WW3D2/pivot.cpp - Enhanced Analysis

## Architectural Role
This file implements the core transformation logic for 3D objects in the SAGE engine's rendering pipeline. PivotClass serves as the fundamental building block for hierarchical object transformations, enabling skeletal animation and object positioning in the game world.

## Cross-References
### Incoming
- Animation system (likely calls `Capture_Update` for bone transformations)
- Object rendering pipeline (uses `PivotClass` for model transformations)
- Scene graph management (relies on pivot hierarchy for parent-child relationships)

### Outgoing
- **WWMath library**: Uses `Matrix3D` operations for transformation math
- **Memory allocation**: Conditionally uses `MSGW3DNEW` for dynamic matrix storage
- **Other pivot instances**: Maintains parent-child relationships through `Parent` pointer

## Design Patterns
- **Composite Pattern**: Pivots form a tree structure where child pivots inherit transformations from parents
- **Flyweight Pattern** (conditional): `LAZY_CAP_MTX_ALLOC` suggests potential optimization for shared matrix storage
- **State Pattern**: Visibility and world-space translation flags modify transformation behavior

*Not inferable*: Exact callers of pivot operations remain unclear without full cross-reference analysis.
