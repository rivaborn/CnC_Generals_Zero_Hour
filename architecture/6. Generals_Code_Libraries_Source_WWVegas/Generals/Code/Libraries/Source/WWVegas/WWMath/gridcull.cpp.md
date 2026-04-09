# Generals/Code/Libraries/Source/WWVegas/WWMath/gridcull.cpp

## Purpose
Implements a spatial partitioning system (grid culling) for efficient object collection based on spatial queries.

## Responsibilities
- Manages a 3D grid for spatial partitioning of cullable objects
- Provides collection methods for objects intersecting points, boxes, or frustums
- Handles object linking/unlinking into grid cells
- Supports serialization of grid parameters
- Maintains statistics for debugging

## Key Types
- GridCullSystemClass (Class): Main grid culling system managing spatial partitioning
- GridLinkClass (Class): Link structure for objects in the grid
- IOGridParametersStruct (Struct): Serialization structure for grid parameters
- (anonymous enum) (Enum): Defines chunk IDs for serialization
- GRID_CHUNK_VERSION/GRID_CHUNK_PARAMETERS (Enum values): Chunk identifiers

## Key Functions
### GridCullSystemClass::Collect_Objects
- Purpose: Collects objects intersecting a spatial query (point/box/frustum)
- Calls: init_volume, collect_objects_in_leaf, map_indices_to_address

### GridCullSystemClass::Re_Partition
- Purpose: Recomputes grid parameters for a given volume
- Calls: Collect_And_Unlink_All, link_object, Get_First/Next_Collected_Object_Internal

### GridCullSystemClass::Save
- Purpose: Serializes grid parameters to a chunk save stream
- Calls: csave.Begin/End_Chunk, csave.Write

### GridCullSystemClass::link_object
- Purpose: Determines grid cell for an object and links it
- Calls: map_point_to_address, link_object_to_list

### collect_objects_in_leaf
- Purpose: Iterates through objects in a grid cell and tests for intersection
- Calls: CollisionMath::Overlap_Test, Add_To_Collection

## Globals
- GRID_CURRENT_VERSION (uint32): Current version of the file format (0x00010000)

## Dependencies
- gridcull.h, chunkio.h, iostruct.h, colmath.h, colmathinlines.h
- GridLinkClass, CullableClass, Vector3, AABoxClass, OBBoxClass, FrustumClass
- CollisionMath, ChunkSaveClass, W3DNEWARRAY, DEFINE_AUTO_POOL
