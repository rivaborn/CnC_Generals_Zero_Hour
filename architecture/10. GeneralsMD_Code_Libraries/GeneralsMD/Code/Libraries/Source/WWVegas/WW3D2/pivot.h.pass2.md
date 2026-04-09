# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/pivot.h - Enhanced Analysis

## Architectural Role
This file defines the core `PivotClass` structure that represents nodes in the W3D engine's scene graph hierarchy. It bridges the rendering pipeline (transform calculations) with animation and user control systems, enabling hierarchical object transformations and visibility management.

## Cross-References
### Incoming
- Animation system (uses `Capture_Update()` and `Is_Captured()` for override control)
- Rendering pipeline (queries `Transform` and `IsVisible` for draw calls)
- Hierarchy traversal code (accesses `Parent` and `BaseTransform` for tree navigation)

### Outgoing
- Matrix/quaternion math (`Matrix3D`, `Quat` for transform operations)
- Memory management (`DynamicMatrix3D` for lazy allocation)
- W3D file I/O (uses `W3D_NAME_LEN` for naming conventions)

## Design Patterns
- **Composite Pattern**: `PivotClass` forms the node structure for hierarchical object composition in the scene graph.
- **State Pattern**: The captured/non-captured state (via `IsCaptured`/`CapTransformPtr`) allows runtime behavior switching between animation-driven and user-controlled transforms.
- **Flyweight (conditional)**: The `LAZY_CAP_MTX_ALLOC` path suggests potential flyweight optimization for transform storage.
