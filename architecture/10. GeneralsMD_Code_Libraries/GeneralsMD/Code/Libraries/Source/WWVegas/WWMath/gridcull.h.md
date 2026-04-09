# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/gridcull.h

## Purpose
Defines a grid-based spatial partitioning system for culling dynamic objects in 3D space.

## Responsibilities
- Implements a grid-based culling system with O(1) insertion
- Manages object linking/unlinking in grid cells
- Provides volume-based collection of objects
- Handles statistics tracking for culling performance
- Supports serialization via ChunkLoad/ChunkSave classes

## Key Types
- **GridCullSystemClass (Class)**: Main grid culling system implementation
- **StatsStruct (Struct)**: Statistics tracking for culling performance
- **VolumeStruct (Struct)**: Defines a volume in the grid for collection
- **TypedGridCullSystemClass (Class)**: Typed wrapper for GridCullSystemClass
- **GridLinkClass (Class)**: Link structure for objects in the grid
- **GridListIterator (Class)**: Iterator for traversing object lists

## Key Functions
### clamp_indices_to_grid
- Purpose: Constrains grid indices to valid range
- Calls: None

### map_point_to_cell
- Purpose: Determines which grid cell contains a point
- Calls: None

### map_point_to_address
- Purpose: Computes grid address for a point
- Calls: map_point_to_cell, map_indices_to_address

### compute_box
- Purpose: Computes bounding box for grid cells
- Calls: None

### init_volume
- Purpose: Initializes volume for various geometric primitives
- Calls: map_point_to_cell, clamp_indices_to_grid

## Globals
- **MinCellSize (Vector3)**: Minimum dimensions for a grid cell
- **MaxObjExtent (float)**: Maximum object size for grid placement
- **TerminationCellCount (int)**: Maximum cells before algorithm terminates
- **Origin (Vector3)**: Grid origin point
- **CellDim (Vector3)**: Dimensions of each grid cell
- **CellCount (int[3])**: Number of cells in each dimension

## Dependencies
- cullsys.h, mempool.h, frustum.h, aabox.h, lineseg.h, obbox.h
- ChunkLoadClass, ChunkSaveClass (forward declarations)
- Vector3, AABoxClass, OBBoxClass, FrustumClass, LineSegClass
