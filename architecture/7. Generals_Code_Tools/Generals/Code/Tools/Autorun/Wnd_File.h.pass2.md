# Generals/Code/Tools/Autorun/Wnd_File.h - Enhanced Analysis

## Architectural Role
This file provides a low-level, cross-platform file I/O abstraction layer used by the Autorun tooling infrastructure. It bridges between the game's higher-level asset loading systems and the underlying OS file APIs, supporting both stream and handle-based backends.

## Cross-References
### Incoming
- Likely called by Autorun tool executables (e.g., `Generals/Code/Tools/Autorun/*.cpp`) for file operations during build/asset processing
- May be referenced by other tooling components needing file I/O abstractions

### Outgoing
- Uses standard C library functions (`fopen`, `fread`, etc.) when `SUPPORT_STREAMS` is enabled
- Uses Windows API (`CreateFile`, `ReadFile`, etc.) when `SUPPORT_HANDLES` is enabled
- Depends on system headers for file statistics and path handling

## Design Patterns
- **Adapter Pattern**: Abstracts different file I/O mechanisms (streams vs handles) behind a unified interface
- **Facade Pattern**: Simplifies complex OS-specific file operations into a cleaner class interface
- **Strategy Pattern**: The choice between stream/handle backends is determined at compile-time via macros, allowing different implementations without changing client code
