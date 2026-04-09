# Generals/Code/Tools/WW3D/max2w3d/geometryexporttask.h

## Purpose
Defines the abstract base class for geometry export tasks in the Max2W3D tool, handling mesh, collision, and other geometry exports.

## Responsibilities
- Provides interface for geometry export tasks
- Manages object naming and hierarchy
- Supports optimization and RTTI for geometry types
- Handles vertex normals and special object detection

## Key Types
- **GeometryExportTaskClass (Class)**: Abstract base for geometry export tasks
- **GeometryExportContextClass (Class)**: Context for export operations (forward declared)
- **GeometryExportTaskClass::GeometryType (Enum)**: RTTI for geometry types (MESH, COLLISIONBOX, DAZZLE, NULLOBJ, AGGREGATE, PROXY)

## Key Functions
### `Export_Geometry`
- Purpose: Pure virtual function to export geometry
- Calls: None (pure virtual)

### `Create_Task`
- Purpose: Factory method to create appropriate task for a node
- Calls: None (static factory)

### `Optimize_Geometry`
- Purpose: Pre-export optimization of geometry tasks
- Calls: None (static optimizer)

### `Get_Shared_Vertex_Normal`
- Purpose: Returns vertex normal for smoothing
- Calls: None (virtual)

### `Is_Aggregate` / `Is_Proxy`
- Purpose: Detects special object types
- Calls: None (virtual)

## Globals
- None

## Dependencies
- `<string.h>`, `<Max.h>`
- `w3d_file.h`, `vector.h`
- `INode`, `Matrix3`, `Point3`, `TimeValue` (3DS Max SDK)
- `DynamicVectorClass` (custom container)
