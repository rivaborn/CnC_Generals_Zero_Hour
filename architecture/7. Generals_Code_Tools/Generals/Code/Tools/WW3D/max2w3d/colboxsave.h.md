# Generals/Code/Tools/WW3D/max2w3d/colboxsave.h

## Purpose
Defines a class for saving collision box data from 3D Studio Max meshes into W3D format.

## Responsibilities
- Encapsulates collision box export functionality
- Handles conversion of Max mesh bounding boxes to W3D format
- Manages progress reporting during export
- Provides error handling via exception codes

## Key Types
- **CollisionBoxSaveClass (Class)**: Main class for collision box export
- **(anonymous enum) (Enum)**: Defines exception error codes
- **EX_UNKNOWN (Enum)**: Unknown error code
- **EX_CANCEL (Enum)**: Cancel operation error code

## Key Functions
### CollisionBoxSaveClass()
- Purpose: Constructor initializing collision box export parameters
- Calls: Not inferable

### Write_To_File()
- Purpose: Writes collision box data to a W3D file chunk
- Calls: Not inferable

## Globals
- None

## Dependencies
- `<Max.h>`: 3D Studio Max SDK
- `"w3d_file.h"`: W3D file format definitions
- `"chunkio.h"`: Chunk I/O utilities
- `"progress.h"`: Progress meter utilities
