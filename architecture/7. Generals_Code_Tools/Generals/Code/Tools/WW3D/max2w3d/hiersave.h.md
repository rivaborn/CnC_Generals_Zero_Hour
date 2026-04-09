# Generals/Code/Tools/WW3D/max2w3d/hiersave.h

## Purpose
Defines classes for saving and loading 3D hierarchy data between Max and W3D formats.

## Responsibilities
- Manages hierarchy node structures and their transforms
- Handles pivot and fixup data for 3D models
- Provides save/load functionality for hierarchy data
- Supports terrain optimization mode

## Key Types
- **HierarchyNodeStruct (struct)**: Contains Max node reference, pivot, and fixup data
- **HierarchySaveClass (class)**: Main class for hierarchy save/load operations
- **MATRIX_FIXUP_* (enum)**: Defines matrix fixup types (none, translation, translation+rotation)

## Key Functions
### HierarchySaveClass()
- Purpose: Constructs hierarchy save object
- Calls: None

### Save()
- Purpose: Saves hierarchy data to chunk stream
- Calls: save_header, save_pivots, save_fixups

### Load()
- Purpose: Loads hierarchy data from chunk stream
- Calls: load_header, load_pivots, load_fixups

### Get_Node_Transform()
- Purpose: Returns world-space transform for a node
- Calls: None

### Get_Fixup_Transform()
- Purpose: Returns fixup matrix for a node
- Calls: fixup_matrix

## Globals
- **TerrainModeEnabled (static bool)**: Controls terrain optimization mode

## Dependencies
- Max SDK headers (Max.h)
- W3D file format headers (w3d_file.h)
- Progress meter (progress.h)
- Chunk I/O (chunkio.h)
- Node list (nodelist.h)
- Vector math (vector.h)
