# Generals/Code/Tools/WW3D/max2w3d/hiersave.cpp

## Purpose
Handles saving and loading 3D hierarchy data (bones, pivots, transforms) for W3D files, used in the Max2W3D export tool.

## Responsibilities
- Manages hierarchy node tree construction and traversal
- Serializes/deserializes hierarchy data to/from W3D file format
- Computes relative transforms and fixup matrices
- Validates bone names for duplicates

## Key Types
- `HierarchySaveClass` (Class): Main class handling hierarchy save/load operations
- `HierarchyNodeStruct` (Struct): Represents a node in the hierarchy with pivot and fixup data
- `W3dPivotStruct` (Struct): Pivot data structure for W3D format
- `W3dPivotFixupStruct` (Struct): Fixup transform structure for W3D format

## Key Functions
### `add_node`
- Purpose: Adds a single node to the hierarchy tree
- Calls: `Set_W3D_Name`, `Find_Named_Node`, `fixup_matrix`, `DecomposeMatrix`, `Cleanup_Orthogonal_Matrix`

### `save_header`
- Purpose: Writes hierarchy header to W3D file
- Calls: `Begin_Chunk`, `Write`, `End_Chunk`

### `load_header`
- Purpose: Reads hierarchy header from W3D file
- Calls: `Read`

### `fixup_matrix`
- Purpose: Conditions a matrix based on fixup type
- Calls: `GetTrans`, `DecomposeMatrix`, `Cleanup_Orthogonal_Matrix`

## Globals
- `TerrainModeEnabled` (bool): Flag for terrain mode state

## Dependencies
- `hiersave.h`, `w3d_file.h`, `nodefilt.h`, `euler.h`, `util.h`, `w3dappdata.h`, `errclass.h`, `exportlog.h`
- `Matrix3`, `Quat`, `Point3`, `INode`, `TimeValue` from 3DS Max SDK
- `W3D_CHUNK_*` constants for chunk identification
