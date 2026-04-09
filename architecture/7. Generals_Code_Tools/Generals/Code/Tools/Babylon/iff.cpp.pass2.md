# Generals/Code/Tools/Babylon/iff.cpp - Enhanced Analysis

## Architectural Role
This file implements the IFF (Interchange File Format) file I/O subsystem, serving as the low-level data serialization layer for toolchain operations. It provides dual-mode access (streaming vs. memory-mapped) for chunked binary data, critical for asset processing pipelines.

## Cross-References
### Incoming
- `CRCDiff.cpp` uses IFF functions for file comparison operations (IFF_Load, IFF_Read, IFF_seek)

### Outgoing
- Directly uses Windows API (_open, _read, _write, lseek)
- Depends on endianness conversion (BgEn32)
- Uses file I/O macros (DO_READ, DO_WRITE) defined elsewhere

## Design Patterns
- **Resource Acquisition Is Initialization (RAII)**: Not implemented - manual memory management with malloc/free
- **Adapter Pattern**: Abstracts file operations to work with both disk files and memory buffers
- **Command Pattern**: DO_READ/WRITE macros encapsulate I/O operations (though implementation is inline)

Key insight: The dual-mode (loaded vs. streaming) design suggests this was optimized for both small configuration files and large asset bundles, with memory mapping used only when necessary.
