# Generals/Code/Tools/WW3D/max2w3d/w3dexp.h - Enhanced Analysis

## Architectural Role
This file defines the core W3D export plugin interface for 3ds Max, bridging the asset pipeline between external 3D tools and the SAGE engine's W3D format. It implements the SceneExport interface and coordinates the export of geometry, animations, and hierarchy data.

## Cross-References
### Incoming
- `max2w3d/w3dexp.cpp` (implementation)
- `max2w3d/dllmain.h` (plugin registration)
- `max2w3d/resource.h` (UI strings)
- 3ds Max SDK headers (`Max.h`, `hiersave.h`)

### Outgoing
- `w3dutil.h` (utility functions)
- `hiersave.h` (hierarchy serialization)
- `MeshConnectionsClass` (geometry connections)
- `GeometryExportTaskClass` (export tasks)

## Design Patterns
- **Adapter Pattern**: Wraps 3ds Max's SceneExport interface to provide W3D-specific export functionality.
- **Facade Pattern**: Provides a simplified interface for complex export operations (hierarchy, animations, LODs).
- **Strategy Pattern**: Export methods (e.g., `Export_Geometry`, `Export_Animation`) can be swapped or extended for different asset types.

*Not inferable*: Exact implementation of progress tracking or error handling.
