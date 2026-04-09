# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/sortingrenderer.h

## Purpose
Declares the `SortingRendererClass` for managing sorted rendering of triangles and volume particles in the SAGE engine.

## Responsibilities
- Manages a sorting pool for deferred rendering
- Provides methods to insert triangles and volume particles with bounding spheres
- Handles flushing of the sorting pool to the GPU
- Controls triangle draw enabling/disabling
- Configures minimum vertex buffer size

## Key Types
- **SortingNodeStruct (Class)**: Not inferable (forward declared).
- **SphereClass (Class)**: Not inferable (forward declared).
- **SortingRendererClass (Class)**: Manages sorted rendering of geometry.

## Key Functions
### `Flush_Sorting_Pool`
- Purpose: Flushes the sorting pool to the GPU.
- Calls: Not inferable.

### `Insert_To_Sorting_Pool`
- Purpose: Inserts a sorting node into the pool.
- Calls: Not inferable.

### `Insert_Triangles` (overload 1)
- Purpose: Inserts triangles with a bounding sphere into the sorting pool.
- Calls: `Insert_To_Sorting_Pool`.

### `Insert_Triangles` (overload 2)
- Purpose: Inserts triangles without a bounding sphere into the sorting pool.
- Calls: `Insert_To_Sorting_Pool`.

### `Insert_VolumeParticle`
- Purpose: Inserts a volume particle with a bounding sphere into the sorting pool.
- Calls: `Insert_To_Sorting_Pool`.

### `Flush`
- Purpose: Flushes all pending rendering commands.
- Calls: `Flush_Sorting_Pool`.

### `Deinit`
- Purpose: Cleans up resources.
- Calls: Not inferable.

### `SetMinVertexBufferSize`
- Purpose:
