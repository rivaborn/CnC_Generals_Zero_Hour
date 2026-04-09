# Generals/Code/Tools/WW3D/max2w3d/util.cpp

## Purpose
Utility functions for 3DS Max to W3D model conversion, handling node names, paths, and geometry checks.

## Responsibilities
- Node name manipulation (splitting, LOD handling)
- Path operations (full/relative path conversion)
- Geometry type detection
- Matrix cleanup for orthogonal matrices
- Damage/Origin node identification

## Key Types
- PathCharType (Enum): Character type in path strings (NULL, SLASH, PLAIN)
- NULL_CHAR (Enum): Null character type
- SLASH_CHAR (Enum): Slash character type
- PLAIN_CHAR (Enum): Plain character type

## Key Functions
### Cleanup_Orthogonal_Matrix
- Purpose: Removes very small numbers from matrix rows and normalizes them
- Calls: None

### Set_W3D_Name
- Purpose: Sets a W3D-compatible name, stripping trailing digits
- Calls: strrchr, sscanf, strupr

### Split_Node_Name
- Purpose: Breaks a node name into base and extension parts
- Calls: strncpy, atoi

### Append_Lod_Character
- Purpose: Appends LOD level to mesh names to avoid conflicts
- Calls: Get_Lod_Level, Find_Named_Node

### Create_Full_Path
- Purpose: Creates full path from current directory and relative path
- Calls: strcpy, strlen

### Create_Relative_Path
- Purpose: Creates relative path from current and full paths
- Calls: malloc, strcpy, strlen, _strupr

### Is_Max_Tri_Mesh
- Purpose: Checks if a node is a triangle mesh
- Calls: EvalWorldState, CanConvertToType

### Is_Damage_Root
- Purpose: Checks if a node is a damage root (parent is scene root, name starts with "damage.")
- Calls: GetParentNode, IsRootNode, GetName

### Is_Origin
- Purpose: Checks if a node is an origin (parent is scene root, name starts with "origin.")
- Calls: GetParentNode, IsRootNode, GetName

### Is_Base_Origin
- Purpose: Checks if a node is the base origin (origin.0 or similar)
- Calls: Is_Origin, GetName, stricmp, sscanf

### Get_Lod_Level
- Purpose: Extracts LOD level from node name
- Calls: GetName, strrchr, atoi

### Get_Damage_State
- Purpose: Extracts damage state from node name
- Calls: Is_Damage_Root, GetName, strrchr, atoi

### Find_Named_Node
- Purpose: Finds a node with a specific name in the hierarchy
- Calls: Set_W3D_Name, GetName, GetChildNode, NumChildren

## Globals
- EPSILON (float): Small value for matrix cleanup threshold
- _string (char[256]): Buffer for string operations

## Dependencies
- util.h, w3dutil.h, skin.h, skindata.h, modstack.h
- INode, INodeListClass, Matrix3, Object classes from 3DS Max SDK
- W3DAppData2Struct class for geometry type retrieval
