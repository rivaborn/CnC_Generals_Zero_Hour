# Generals/Code/Tools/WW3D/max2w3d/maxworldinfo.h

## Purpose
Provides scene-wide information for the Max2W3D plugin, enabling mesh smoothing across adjacent meshes.

## Responsibilities
- Manages export tasks and scene state during conversion
- Handles shared vertex normals for mesh smoothing
- Tracks current export transform and time
- Controls mesh smoothing behavior

## Key Types
- **MaxWorldInfoClass (Class)**: Wraps 3DS Max scene info for W3D export
- **GeometryExportTaskClass (Class)**: Reference to mesh export tasks (defined elsewhere)

## Key Functions
### MaxWorldInfoClass()
- Purpose: Constructor initializing mesh list and default settings
- Calls: None

### Get_Shared_Vertex_Normal()
- Purpose: Retrieves smoothed normal for shared vertices
- Calls: Not inferable

### Set_Current_Task()
- Purpose: Sets the currently active export task
- Calls: None

### Allow_Mesh_Smoothing()
- Purpose: Enables/disables cross-mesh normal smoothing
- Calls: None

## Globals
- **MeshList (DynamicVectorClass<GeometryExportTaskClass*>&)**: Reference to all export tasks
- **CurrentTask (GeometryExportTaskClass*)**: Currently active export task
- **CurrentTime (TimeValue)**: Scene time during export
- **ExportTrans (Matrix3)**: Transform applied during export
- **SmoothBetweenMeshes (bool)**: Flag for mesh smoothing

## Dependencies
- `<Max.h>` (3DS Max SDK)
- `"meshbuild.h"` (local mesh export infrastructure)
- `"nodelist.h"` (node management)
- `"vector.h"` (math utilities)
- `WorldInfoClass` (base class from 3DS Max SDK)
- `TimeValue`, `Matrix3` (3DS Max types
