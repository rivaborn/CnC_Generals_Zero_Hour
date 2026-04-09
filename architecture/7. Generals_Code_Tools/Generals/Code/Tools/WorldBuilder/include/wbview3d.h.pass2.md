# Generals/Code/Tools/WorldBuilder/include/wbview3d.h - Enhanced Analysis

## Architectural Role
This header defines the core 3D rendering interface for WorldBuilder, bridging the editor UI with the W3D rendering pipeline. It encapsulates camera control, object selection, and view transformations while managing DirectX resource lifecycle.

## Cross-References
### Incoming
- `CWorldBuilderView` (main editor view) likely calls `redraw()`, `picked3dObjectInView()`, and coordinate conversion methods
- `WBHeightMap` and `LayerClass` implementations use `invalObjectInView()` for dirty region management
- `MapObject` and `BuildListInfo` classes rely on `getBestModelName()` for asset resolution

### Outgoing
- Directly uses `DX8_CleanupHook` for resource management
- Interacts with `W3DAssetManager` for model loading
- Depends on `CameraClass` and `LightClass` for scene setup
- Calls into `SkeletonSceneClass` for hierarchical rendering

## Design Patterns
- **Facade Pattern**: Exposes simplified 3D rendering operations while hiding W3D complexity
- **Observer Pattern**: Uses `invalObjectInView()` to notify render system of changes (implicit subscription)
- **Strategy Pattern**: Different camera modes (top-down vs. isometric) are selectable strategies

*Not inferable*: Exact implementation of `IntersectionClass` usage or threading model.
