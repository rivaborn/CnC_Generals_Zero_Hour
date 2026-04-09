# Generals/Code/Tools/WW3D/max2w3d/util.h

## Purpose
Header file providing utility functions for 3D model export from 3ds Max to W3D format.

## Responsibilities
- Matrix cleanup utilities
- Node naming and path manipulation
- Triangle mesh detection
- Origin and damage state handling
- LOD level management

## Key Types
None

## Key Functions
### Cleanup_Orthogonal_Matrix
- Purpose: Removes very small numbers from a matrix by setting them to zero.
- Calls: None

### Set_W3D_Name
- Purpose: Sets a W3D-compatible name from a source string.
- Calls: None

### Split_Node_Name
- Purpose: Splits a node name into base and extension components.
- Calls: None

### Append_Lod_Character
- Purpose: Appends LOD level character to mesh name.
- Calls: None

### Create_Full_Path
- Purpose: Creates full path from current working directory and relative path.
- Calls: None

### Create_Relative_Path
- Purpose: Creates relative path from full path and current working directory.
- Calls: None

### Is_Full_Path
- Purpose: Checks if a path is a full path.
- Calls: None

### Is_Max_Tri_Mesh
- Purpose: Determines if a node is a triangle mesh in 3ds Max.
- Calls: None

### Is_Origin
- Purpose: Checks if a node is an origin node.
- Calls: None

### Is_Base_Origin
- Purpose: Checks if a node is a base origin node.
- Calls: None

### Find_Origin
- Purpose: Finds the origin node in a hierarchy.
- Calls: None

### Is_Damage_Root
- Purpose: Checks if
