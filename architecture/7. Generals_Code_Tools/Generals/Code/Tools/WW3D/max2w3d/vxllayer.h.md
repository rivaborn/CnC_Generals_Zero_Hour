# Generals/Code/Tools/WW3D/max2w3d/vxllayer.h

## Purpose
Defines the VoxelLayerClass for voxel-based object rendering in the 3DS Max to W3D exporter tool.

## Responsibilities
- Manages voxel layer visibility and solidity state
- Handles voxel bitmap operations (lines, triangles)
- Provides intersection and scan conversion for voxel slices
- Tracks voxel layer dimensions and slice parameters

## Key Types
- VoxelLayerClass (Class): Manages voxel layer data and operations
- VOXEL_VISIBLE (const sint8): Voxel state constant (outside object)
- VOXEL_SOLID (const sint8): Voxel state constant (part of object)
- VOXEL_UNKNOWN (const sint8): Voxel state constant (unknown state)

## Key Functions
### VoxelLayerClass()
- Purpose: Default constructor for VoxelLayerClass
- Calls: None

### VoxelLayerClass(INodeListClass &, TimeValue, Matrix3, Point3, Point3, float, float, int, int)
- Purpose: Constructs voxel layer from 3DS Max scene data
- Calls: None

### Is_Visible(int, int)
- Purpose: Checks if a voxel at (x,y) is visible
- Calls: None

### Is_Solid(int, int)
- Purpose: Checks if a voxel at (x,y) is solid
- Calls: None

### Set_Visible(int, int)
- Purpose: Marks a voxel as visible
- Calls: None

### Add_Solid(int, int)
- Purpose: Marks a voxel as solid
- Calls: None

### Draw_Line(double, double, double, double)
- Purpose: Draws a line of voxels in the bitmap
- Calls: None
