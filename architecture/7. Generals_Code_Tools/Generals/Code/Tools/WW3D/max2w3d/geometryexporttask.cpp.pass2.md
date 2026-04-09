# Generals/Code/Tools/WW3D/max2w3d/geometryexporttask.cpp - Enhanced Analysis

## Architectural Role
This file is part of the Max2W3D toolchain, bridging 3ds Max and the W3D format. It implements geometry export tasks that optimize and convert 3D assets into the engine's proprietary format, handling mesh splitting, combining, and material management.

## Cross-References
### Incoming
- **max2w3d/geometryexportcontext.cpp**: Uses `GeometryExportTaskClass` hierarchy for export orchestration
- **max2w3d/maxworldinfo.cpp**: References `GeometryExportTaskClass` for world export context
- **max2w3d/meshsave.cpp**: Depends on `MeshGeometryExportTaskClass` for mesh data access

### Outgoing
- **max2w3d/meshsave.cpp**: Calls `MeshSaveClass` for W3D mesh serialization
- **max2w3d/colboxsave.cpp**: Uses `CollisionBoxGeometryExportTaskClass` for collision export
- **max2w3d/dazzlesave.cpp**: Leverages `DazzleGeometryExportTaskClass` for dazzle effects
- **max2w3d/hiersave.cpp**: Relies on `AggregateGeometryExportTaskClass` for hierarchy management

## Design Patterns
- **Factory Pattern**: `Create_Task` virtual method enables polymorphic task creation
- **Composite Pattern**: `AggregateGeometryExportTaskClass` manages collections of export tasks
- **Strategy Pattern**: Different export task classes encapsulate varying export behaviors

*Not inferable*: Exact implementation of optimization heuristics (e.g., face count limits)
