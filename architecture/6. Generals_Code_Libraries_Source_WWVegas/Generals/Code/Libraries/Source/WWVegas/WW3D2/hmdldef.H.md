# Generals/Code/Libraries/Source/WWVegas/WW3D2/hmdldef.H

## Purpose
Defines the `HModelDefClass` and related structures for hierarchy model definitions in the SAGE engine.

## Responsibilities
- Defines the `HmdlNodeDefStruct` for render object attachments.
- Implements `HModelDefClass` as a blueprint for hierarchy models.
- Handles loading of W3D hierarchy model definitions.
- Manages sub-objects, snap points, and model metadata.

## Key Types
- `HmdlNodeDefStruct` (struct): Associates a named render object with a pivot/bone in the hierarchy tree.
- `HModelDefClass` (class): Blueprint for creating hierarchy models, storing model definitions and loading W3D files.

## Key Functions
### `Load_W3D`
- Purpose: Loads a W3D hierarchy model definition from a chunk loader.
- Calls: `read_header`, `read_connection`, `read_mesh_connection`, `read_collision_connection`, `read_skin_connection`.

### `read_header`
- Purpose: Reads the header information of the W3D file.
- Calls: Not inferable.

### `read_connection`
- Purpose: Reads connection data for sub-objects.
- Calls: Not inferable.

### `read_mesh_connection`
- Purpose: Reads mesh connection data.
- Calls: Not inferable.

### `read_collision_connection`
- Purpose: Reads collision connection data.
- Calls: Not inferable.

### `read_skin_connection`
- Purpose: Reads skin connection data.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `always.h`, `w3d_file.h`
- `FileClass`, `ChunkLoadClass`, `ChunkSaveClass`, `SnapPointsClass` (forward declarations)
