# Generals/Code/Libraries/Source/WWVegas/WWLib/rawfile.cpp - Enhanced Analysis

## Architectural Role
This file provides the core cross-platform file I/O abstraction layer for the SAGE engine, handling low-level file operations with bias support for virtual file offsets. It serves as the foundation for all file operations across the engine, including asset loading, save/load functionality, and modding infrastructure.

## Cross-References
### Incoming
- Asset loading systems (e.g., W3D model loader, texture manager)
- Save/load game functionality
- Modding infrastructure (INI file handling, custom asset loading)
- Networking code (for file transfers in multiplayer)

### Outgoing
- Platform-specific file APIs (Win32 API or POSIX)
- Memory management system (for buffer allocations)
- Error reporting system (for file operation failures)

## Design Patterns
- **Wrapper Facade**: Abstracts platform-specific file operations behind a unified interface
- **Bias Pattern**: Implements virtual file offsets to support memory-mapped or compressed file access
- **Error Handling Strategy**: Centralized error reporting with retry capability

Rules followed. Output under 400 tokens.
