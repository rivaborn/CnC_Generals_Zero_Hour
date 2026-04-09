# Generals/Code/Tools/WW3D/max2w3d/TARGA.CPP - Enhanced Analysis

## Architectural Role
This file is part of the WW3D (Westwood 3D) toolchain, specifically handling TGA image file I/O for the max2w3d converter tool. It bridges between the game's asset pipeline and the 3D modeling workflow, enabling artists to export TGA textures for use in the W3D format.

## Cross-References
### Incoming
- Likely called by `max2w3d` tool's asset processing pipeline
- Potentially referenced by other WW3D tools needing TGA support

### Outgoing
- Uses WWLib's `FileClass`/`FileFactory` for file I/O (when `TGA_USES_WWLIB_FILE_CLASSES` is defined)
- Falls back to standard C I/O (`stdio.h`, `fcntl.h`) for non-WWLib builds

## Design Patterns
- **Adapter Pattern**: Abstracts file I/O operations behind platform-specific implementations
- **Resource Management**: Explicit memory allocation/deallocation for image/palette buffers
- **Error Handling**: Centralized error reporting via `Targa_Error_Handler`

*Not inferable*: No clear use of Factory, Observer, or other complex patterns.
