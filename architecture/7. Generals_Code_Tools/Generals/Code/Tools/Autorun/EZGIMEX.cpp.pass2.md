# Generals/Code/Tools/Autorun/EZGIMEX.cpp - Enhanced Analysis

## Architectural Role
This file provides low-level I/O abstractions for the GIMAX library, serving as a bridge between the engine's memory/file operations and the underlying C runtime. It's part of the toolchain infrastructure, likely used during build/asset processing rather than runtime.

## Cross-References
### Incoming
- Not inferable (no callers visible in this file)

### Outgoing
- Calls into C runtime (`malloc`, `free`, `fopen`, `fread`, etc.)
- Uses `Msg` from `wnd_file.h` for logging

## Design Patterns
- **Adapter Pattern**: Wraps C runtime functions (`fopen`, `fread`, etc.) to provide a consistent interface for file operations.
- **Byte Order Conversion**: Uses `ggetm`/`gputm` and `ggeti`/`gputi` for endianness handling, critical for cross-platform binary data.
- **Resource Tracking**: Global `galloccount` tracks memory allocations, hinting at debug/leak detection tools.
