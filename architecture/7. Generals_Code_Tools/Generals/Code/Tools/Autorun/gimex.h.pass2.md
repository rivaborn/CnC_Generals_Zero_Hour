# Generals/Code/Tools/Autorun/gimex.h - Enhanced Analysis

## Architectural Role
This header defines the GIMEX (Graphics IMport EXport) API, serving as the core abstraction layer for bitmap file I/O and memory management in the SAGE engine's toolchain. It bridges low-level file operations with higher-level graphics asset handling, particularly for the Autorun tool used in content generation.

## Cross-References
### Incoming
- **Generals/Code/Tools/Autorun/gimex.cpp**: Implements the functions declared here
- **Generals/Code/Tools/Autorun/autorun.cpp**: Likely uses GIMEX for asset processing
- **W3D importers/exporters**: Would call GIMEX functions for bitmap handling

### Outgoing
- **Platform-specific I/O**: Uses system file APIs (not directly visible here)
- **Memory allocation**: Likely calls `malloc`/`free` or engine-specific allocators
- **Watcom assembly**: Directly includes inline assembly for performance-critical ops

## Design Patterns
- **Facade Pattern**: GIMEX abstracts complex file formats and platform-specific details behind a unified API
- **Adapter Pattern**: Handles platform-specific ARGB layouts (Mac vs. PC) via preprocessor directives
- **Resource Management**: `GSTREAM` and `GINSTANCE` act as resource handles for RAII-like control (though C-based)

**Key Insight**: The Watcom-specific inline assembly for `ggeti`/`ggetm` reveals performance optimization for little-endian byte order handling, critical for cross-platform bitmap operations. This suggests GIMEX was designed for both PC and Mac builds.
