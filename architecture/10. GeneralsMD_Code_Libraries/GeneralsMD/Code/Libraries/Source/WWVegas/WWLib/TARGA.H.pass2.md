# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/TARGA.H - Enhanced Analysis

## Architectural Role
This file defines the core TGA image handling infrastructure in the SAGE engine, bridging low-level file I/O with the rendering pipeline. It abstracts TGA file operations, supporting both legacy I/O and WWLib's FileClass system, making it a critical dependency for texture loading across the engine.

## Cross-References
### Incoming
- Rendering subsystem (W3D) - Uses Targa for texture loading
- Asset loading pipeline - Calls Load/Save for TGA assets
- UI system - Likely uses TGA for menu graphics

### Outgoing
- File I/O subsystem (FileClass or stdio) - Core dependency
- Memory allocation system - For image/palette buffers
- Error handling framework - Uses TARGA_ERROR_HANDLER macro

## Design Patterns
- **Adapter Pattern**: Abstracts between stdio and FileClass I/O
- **Facade Pattern**: Simplifies complex TGA format operations
- **Strategy Pattern**: Different encoding/decoding strategies for compressed/uncompressed TGA

*Not inferable*: Exact compression algorithm implementation details.
