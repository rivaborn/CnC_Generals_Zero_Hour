# Generals/Code/Tools/WW3D/max2w3d/dazzlesave.h

## Purpose
Defines the `DazzleSaveClass` for exporting dazzle effects from 3DS Max to W3D format.

## Responsibilities
- Encapsulates dazzle effect export logic
- Handles transform and dazzle type serialization
- Integrates with 3DS Max SDK (`INode`, `Matrix3`)
- Uses W3D file I/O infrastructure
- Provides progress meter feedback

## Key Types
- **DazzleSaveClass (Class)**: Manages dazzle effect export from 3DS Max nodes.
- **(anonymous enum) (Enum)**: Defines exception error codes for export failures.
- **EX_UNKNOWN (Enum)**: Unknown error code.
- **EX_CANCEL (Enum)**: User cancellation error code.

## Key Functions
### DazzleSaveClass (Constructor)
- Purpose: Initializes dazzle export with node and transform data.
- Calls: Not inferable (constructor body not shown).

### Write_To_File
- Purpose: Serializes dazzle data to a W3D chunk file.
- Calls: `ChunkSaveClass` methods (parameter `csave`).

## Globals
- None

## Dependencies
- `<Max.h>` (3DS Max SDK)
- `"w3d_file.h"` (W3D file I/O)
- `"chunkio.h"` (Chunk-based I/O)
- `"progress.h"` (Progress meter)
- `INode`, `Matrix3`, `TimeValue` (3DS Max types)
- `ChunkSaveClass` (external class for chunk saving)
