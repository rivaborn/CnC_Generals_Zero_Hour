# Generals/Code/Tools/WW3D/max2w3d/vxl.h

## Purpose
Defines the `VoxelClass` for computing physical properties of 3D meshes using voxelization.

## Responsibilities
- Voxelize polygon meshes for physics calculations
- Compute moment of inertia, center of mass, and volume
- Manage voxel grid visibility and spatial queries
- Handle mesh quantization and bounding box calculations

## Key Types
- **VoxelClass (Class)**: Manages voxel grid and physics property calculations for 3D meshes.

## Key Functions
### VoxelClass()
- Purpose: Constructs voxel grid from mesh list and resolution.
- Calls: `Quantize_Meshes`, `Compute_Bounding_Box`, `Compute_Visiblity`

### Compute_Physical_Properties()
- Purpose: Calculates volume, center of mass, and moment of inertia tensor.
- Calls: Not inferable (implementation in .cpp)

### Quantize_Meshes()
- Purpose: Converts meshes into voxel grid representation.
- Calls: Not inferable (implementation in .cpp)

### Compute_Visiblity()
- Purpose: Computes 3D visibility for voxel grid.
- Calls: Not inferable (implementation in .cpp)

## Globals
- None

## Dependencies
- `always.h`, `Max.h`, `nodelist.h`, `vxllayer.h`, `progress.h`
- `INodeListClass`, `VoxelLayerClass`, `Progress_Meter_Class`, `Matrix3`, `Point3`, `TimeValue`
