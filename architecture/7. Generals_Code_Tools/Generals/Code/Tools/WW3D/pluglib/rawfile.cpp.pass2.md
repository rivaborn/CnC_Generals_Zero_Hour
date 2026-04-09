# Generals/Code/Tools/WW3D/pluglib/rawfile.cpp - Enhanced Analysis

## Architectural Role
This file provides the core file I/O abstraction layer for the SAGE engine's toolchain, enabling cross-platform file operations with bias support for asset processing. It serves as the foundation for all file operations in the WW3D plugin library.

## Cross-References
### Incoming
- Asset processing tools (e.g., model/animation converters)
- WW3D plugin system (uses RawFileClass for resource loading)
- Build pipeline tools (for packaging game assets)

### Outgoing
- Windows API (SetFilePointer, GetFileInformationByHandle)
- POSIX API (fseek, stat) for Unix compatibility
- Standard C library (stdio.h, stdlib.h) for basic operations

## Design Patterns
- **Wrapper Facade**: Abstracts platform-specific file I/O behind a unified interface
- **Bias Pattern**: Implements artificial file boundaries for constrained access (e.g., embedded resources)
- **Error Handling Strategy**: Centralized error reporting via Error() method

*Not inferable*: Specific usage patterns in asset pipeline tools.
