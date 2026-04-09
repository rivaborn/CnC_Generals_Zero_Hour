# GeneralsMD/Code/Libraries/Source/Compression/EAC/gimex.h - Enhanced Analysis

## Architectural Role
This header defines the GIMEX API, a cross-platform graphics import/export system used throughout the engine for texture and image handling. It serves as the abstraction layer between the game's rendering pipeline (W3D) and various image formats, enabling consistent image operations across different platforms.

## Cross-References
### Incoming
- **W3D Rendering System**: Uses GIMEX for texture loading and management
- **Asset Pipeline Tools**: Likely consumes GIMEX for image conversion/export
- **UI System**: May use GIMEX for loading UI graphics

### Outgoing
- **Platform-Specific Implementations**: Function pointers in `GFUNCTIONS` delegate to platform-specific code
- **Memory Allocation**: Uses `malloc`/`free` for buffer management
- **File I/O**: Relies on underlying file system for stream operations

## Design Patterns
- **Bridge Pattern**: `GFUNCTIONS` table decouples interface from implementation, allowing different backends
- **Facade Pattern**: Provides simplified API for complex image operations
- **Inline Functions**: `ggetm/ggeti` and `gputm/gputi` optimize cross-platform memory access without function call overhead

*Not inferable*: Exact usage patterns in calling code (e.g., threading model, error handling).
