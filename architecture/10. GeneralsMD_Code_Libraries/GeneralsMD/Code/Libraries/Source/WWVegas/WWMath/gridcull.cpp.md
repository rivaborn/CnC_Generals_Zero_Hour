# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/gridcull.cpp

## Purpose
Implements a spatial partitioning system (grid culling) for efficient object culling in 3D space.

## Responsibilities
- Manages a 3D grid for spatial partitioning of cullable objects
- Provides collection methods for objects intersecting with points, boxes, or frustums
- Handles object linking/unlinking into grid cells
- Supports serialization of grid parameters
- Maintains statistics for debugging

## Key Types
- `(anonymous enum)` (Enum): Chunk ID constants for file I/O
- `GRID_CHUNK_VERSION` (Enum): Version chunk identifier
- `GRID_CHUNK_PARAMETERS` (Enum): Parameters chunk identifier
- `IOGridParametersStruct` (Class): Structure for saving/loading grid parameters
- `GridLinkClass` (Class): Link object for managing object connections in grid cells
- `GridCullSystemClass` (Class): Main grid culling system class

## Key Functions
### `GridCullSystemClass::Collect_Objects`
- Purpose: Collects objects intersecting with a point, AABox, OBBox, or frustum
- Calls: `init_volume`, `collect_objects_in_leaf`, `map_indices_to_address`

### `GridCullSystemClass::Re_Partition`
- Purpose: Recomputes grid parameters for a given volume
- Calls: `Collect_And_Unlink_All`, `link_object`

### `GridCullSystemClass::Save`
- Purpose: Serializes grid parameters to a chunk file
- Calls: `csave.Begin_Chunk`, `csave.Write`, `csave.End_Chunk`

### `GridCullSystemClass::link_object`
- Purpose: Determines grid cell for an object and links it
- Calls: `map_point_to_address`, `link_object_to_list`

### `collect_objects_in_leaf`
- Purpose: Collects objects from a grid cell that intersect with a volume
- Calls: `Add_To_Collection`, `CollisionMath::Overlap_Test`

## Globals
- `GRID_CURRENT_VERSION` (uint32): Current version of the file format (0x00010000)

## Dependencies
- `gridcull.h`, `chunkio.h`, `iostruct.h`, `colmath.h`, `colmathinlines.h`
- `Vector3`, `AABoxClass`, `OBBoxClass`, `FrustumClass`, `CullableClass`, `GridLinkClass`
- `CollisionMath` namespace for overlap testing
- `W3DNEWARRAY` for memory allocation
