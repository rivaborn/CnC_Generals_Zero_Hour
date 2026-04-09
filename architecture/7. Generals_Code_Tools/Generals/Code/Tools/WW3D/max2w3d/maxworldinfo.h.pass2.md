# Generals/Code/Tools/WW3D/max2w3d/maxworldinfo.h - Enhanced Analysis

## Architectural Role
This file defines the bridge between 3DS Max's scene graph and the W3D export pipeline, enabling cross-mesh operations during model conversion. It's part of the asset pipeline tooling that transforms Max scenes into the engine's proprietary format.

## Cross-References
### Incoming
- `meshbuild.cpp` (uses `MaxWorldInfoClass` for smoothing operations)
- `max2w3d.cpp` (initializes and configures the world info during export)
- Other Max plugin callbacks (access scene state via this class)

### Outgoing
- Calls into `GeometryExportTaskClass` methods (task management)
- Uses `Vector3` and `Matrix3` from 3DS Max SDK (math operations)
- Relies on `WorldInfoClass` virtual methods (base class overrides)

## Design Patterns
- **Adapter Pattern**: Wraps 3DS Max's `WorldInfoClass` to expose W3D-specific functionality
- **Context Object**: Maintains export state (transform, time, current task) for the pipeline
- **Strategy Pattern**: `SmoothBetweenMeshes` flag allows runtime selection of smoothing behavior

*Not inferable*: Exact relationship with `GeometryExportTaskClass` hierarchy.
