# Generals/Code/Tools/WW3D/max2w3d/vxl.cpp

## Purpose
Handles voxelization of 3D meshes for physics calculations (volume, center of mass, inertia tensor).

## Responsibilities
- Computes mesh bounding box and dimensions
- Voxelizes meshes into a 3D grid
- Calculates visibility (outer shell) of voxelized object
- Computes physical properties (volume, center of mass, inertia tensor)

## Key Types
- **VoxelClass (Class)**: Main voxelization class managing voxel data and calculations
- **VoxelLayerClass (Class)**: Represents a 2D slice of voxel data (referenced but not defined here)
- **INodeListClass (Class)**: List of 3D nodes/meshes (external)
- **Progress_Meter_Class (Class)**: Progress tracking (external)

## Key Functions
### `compute_dimensions`
- Purpose: Calculates min/max bounds and surface area of mesh list
- Calls: `meshlist.Num_Nodes()`, `n->EvalWorldState()`, `obj->ConvertToType()`, `mesh->getNumVerts()`, `mesh->getNumFaces()`

### `VoxelClass::Quantize_Meshes`
- Purpose: Converts mesh list into voxel grid data
- Calls: `VoxelLayerClass` constructor, `Set_Layer()`, `Compute_Visiblity()`, `Compute_Bounding_Box()`

### `VoxelClass::Compute_Visiblity`
- Purpose: Marks outer shell voxels as visible via tunneling algorithm
- Calls: `raw_read_vis()`, `raw_set_vis()`

### `VoxelClass::Compute_Physical_Properties`
- Purpose: Calculates volume, center of mass, and inertia tensor from voxel data
- Calls: `Is_Solid()`, `Voxel_Position()`

## Globals
- **VIS_UNKNOWN (const int)**: Unknown voxel state (0)
- **VIS_SOLID (const int)**: Solid voxel state (1)
- **VIS_VISIBLE (const int)**: Visible voxel state (2)

## Dependencies
- Key includes: `vxl.h`, `errclass.h`
- External symbols: `INodeListClass`, `Progress_Meter_Class`, `Matrix3`, `Point3`, `TriObject`, `Mesh`, `Face`
