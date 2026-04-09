# Generals/Code/Tools/WW3D/max2w3d/geometryexporttask.cpp

## Purpose
Handles geometry export tasks for converting 3D models from 3ds Max to W3D format, including mesh, collision, dazzle, and aggregate objects.

## Responsibilities
- Defines export task classes for different geometry types
- Implements mesh optimization (splitting, combining)
- Manages material handling and bounding box calculations
- Provides vertex normal smoothing support
- Handles progress tracking during export

## Key Types
- **MeshGeometryExportTaskClass (Class)**: Handles mesh export with material optimization
- **CollisionBoxGeometryExportTaskClass (Class)**: Exports collision boxes
- **DazzleGeometryExportTaskClass (Class)**: Exports dazzle effects
- **NullGeometryExportTaskClass (Class)**: Creates NULL objects in hierarchy
- **AggregateGeometryExportTaskClass (Class)**: Handles external W3D object references
- **ProxyExportTaskClass (Class)**: Manages game object instantiation proxies

## Key Functions
### MeshGeometryExportTaskClass::Export_Geometry
- Purpose: Exports mesh geometry to W3D format
- Calls: MeshSaveClass constructor, Write_To_File

### MeshGeometryExportTaskClass::Split
- Purpose: Splits multi-material meshes into single-material meshes
- Calls: Reduce_To_Single_Material

### MeshGeometryExportTaskClass::Combine_Mesh
- Purpose: Merges two meshes into one
- Calls: CombineMeshes

### MeshGeometryExportTaskClass::Get_Shared_Vertex_Normal
- Purpose: Calculates smoothed vertex normals
- Calls: None (uses basic math operations)

## Globals
- **OPTIMIZATION_FACECOUNT_LIMIT (int)**: Maximum faces before optimization stops (256)
- **OPTIMIZATION_COMBINING_DISTANCE (float)**: Maximum distance for mesh combining (20.0f)

## Dependencies
- geometryexporttask.h, geometryexportcontext.h, util.h, w3dutil.h
- w3dappdata.h, hiersave.h, maxworldinfo.h, meshsave.h
- colboxsave.h, dazzlesave.h, <bitarray.h>
- External: INode, Mtl, Matrix3, Point3, Box3 classes
