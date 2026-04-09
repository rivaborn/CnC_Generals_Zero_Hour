# Generals/Code/Tools/WW3D/max2w3d/maxworldinfo.cpp

## Purpose
Handles shared vertex normal calculations across meshes in a 3D world during export from 3ds Max to W3D format.

## Responsibilities
- Calculates vertex normals for shared vertices across meshes
- Applies smoothing groups to normal computation
- Uses world transformation matrices for position accuracy
- Iterates through all meshes in the scene

## Key Types
- `MaxWorldInfoClass` (Class): Manages world-level geometry export data and operations
- `GeometryExportTaskClass` (Class): Represents individual mesh export tasks

## Key Functions
### `Get_Shared_Vertex_Normal`
- Purpose: Computes a shared vertex normal by aggregating normals from all meshes containing the vertex in the same smoothing group
- Calls: `GeometryExportTaskClass::Get_Shared_Vertex_Normal`

## Globals
- `ExportTrans` (Matrix): World transformation matrix for position conversion
- `MeshList` (Array): List of all geometry export tasks in the scene
- `CurrentTask` (GeometryExportTaskClass*): Pointer to the currently processed mesh task

## Dependencies
- `maxworldinfo.h`: Header for MaxWorldInfoClass
- `geometryexporttask.h`: Header for GeometryExportTaskClass
- `Vector3`, `Point3`: 3D math types
- `Matrix`: Transformation matrix type
