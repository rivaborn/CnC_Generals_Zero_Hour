# Generals/Code/Libraries/Source/WWVegas/WW3D2/sortingrenderer.h

## Purpose
Declares the `SortingRendererClass` for managing sorted rendering of triangles and volume particles in the SAGE engine.

## Responsibilities
- Manages a sorting pool for deferred rendering
- Handles insertion of triangles and volume particles with bounding spheres
- Controls flushing of the sorting pool to the GPU
- Provides configuration for triangle draw enabling/disabling

## Key Types
- **SortingNodeStruct (Class)**: Not inferable (forward declared).
- **SphereClass (Class)**: Not inferable (forward declared).
- **SortingRendererClass (Class)**: Manages sorted rendering of geometry.

## Key Functions
### `Insert_Triangles` (overloads)
- Purpose: Inserts triangles into the sorting pool with or without a bounding sphere.
- Calls: `Insert_To_Sorting_Pool`

### `Insert_VolumeParticle`
- Purpose: Inserts volume particles into the sorting pool with a bounding sphere.
- Calls: `Insert_To_Sorting_Pool`

### `Flush`
- Purpose: Renders all sorted geometry in the pool.
- Calls: `Flush_Sorting_Pool`

### `Flush_Sorting_Pool`
- Purpose: Internal method to flush the sorting pool.
- Calls: Not inferable.

### `Insert_To_Sorting_Pool`
- Purpose: Internal method to add nodes to the sorting pool.
- Calls: Not inferable.

### `_Enable_Triangle_Draw`
- Purpose: Enables/disables triangle drawing.
- Calls: None.

### `_Is_Triangle_Draw_Enabled`
- Purpose: Checks if triangle drawing is enabled.
- Calls: None.

## Globals
- **_EnableTriangleDraw (bool)**: Tracks whether triangle drawing is enabled.

## Dependencies
- `always.h` (
