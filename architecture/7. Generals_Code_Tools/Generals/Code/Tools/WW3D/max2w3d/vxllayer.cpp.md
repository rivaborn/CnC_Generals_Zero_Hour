# Generals/Code/Tools/WW3D/max2w3d/vxllayer.cpp

## Purpose
Handles voxel layer generation by clipping and scan-converting triangles into a voxel slab for 3D model export.

## Responsibilities
- Clips triangles against voxel slab boundaries
- Scan-converts triangles into voxel space
- Renders lines of voxels into the slab
- Manages scanline table for polygon rendering
- Handles barycentric coordinate calculations

## Key Types
- `vertexstruct` (Class): Stores position and barycentric coordinates for vertices
- `scanstruct` (Class): Contains left/right edge information for scanline conversion
- `PlaneClass` (External): Used for clipping operations (from plane.h)

## Key Functions
### `clip_tri_to_slab`
- Purpose: Clips a triangle against a voxel slab's Z boundaries
- Calls: `clip_poly`, `PlaneClass` constructor

### `clip_poly`
- Purpose: Clips a polygon against a single 3D plane
- Calls: `inside`, `intersect`, `output`

### `scan_edge`
- Purpose: Scan converts an edge into the scanline table
- Calls: None (uses global `_scantab`)

### `fixup_scan_table`
- Purpose: Ensures scanline spans are left-to-right and gap-free
- Calls: None

## Globals
- `_scantab` (scanstruct[256]): Static scanline table for polygon rendering
- `LEFT` (int): Constant for left edge identifier
- `RIGHT` (int): Constant for right edge identifier
- `EMPTY_SPAN` (float): Sentinel value for empty scanline entries

## Dependencies
- `vxllayer.h`: Header for VoxelLayerClass
- `plane.h`: For PlaneClass used in clipping operations
- MAX SDK types (INode, Object, TriObject, Mesh, etc.)
