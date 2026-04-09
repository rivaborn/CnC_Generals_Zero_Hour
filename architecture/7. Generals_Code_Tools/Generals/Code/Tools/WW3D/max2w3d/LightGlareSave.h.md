# Generals/Code/Tools/WW3D/max2w3d/LightGlareSave.h

## Purpose
Defines a class for exporting light glare data from 3DS Max to a W3D file format.

## Responsibilities
- Encapsulates light glare export functionality
- Handles conversion of Max mesh data to W3D format
- Manages progress reporting during export
- Provides error handling via exception codes

## Key Types
- **LightGlareSaveClass (Class)**: Main class handling light glare export
- **(anonymous enum) (Enum)**: Defines exception error codes
- **EX_UNKNOWN (Enum)**: Unknown error code
- **EX_CANCEL (Enum)**: Cancel operation error code

## Key Functions
### LightGlareSaveClass
- Purpose: Constructor initializing light glare export parameters
- Calls: Not inferable

### Write_To_File
- Purpose: Writes light glare data to a chunk save file
- Calls: Not inferable

## Globals
- None

## Dependencies
- `<Max.h>`: 3DS Max SDK
- `"w3d_file.h"`: W3D file format definitions
- `"chunkio.h"`: Chunk I/O utilities
- `"progress.h"`: Progress meter class
