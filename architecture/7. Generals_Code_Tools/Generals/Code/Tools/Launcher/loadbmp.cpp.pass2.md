# Generals/Code/Tools/Launcher/loadbmp.cpp - Enhanced Analysis

## Architectural Role
This file is part of the launcher tool's UI subsystem, responsible for loading and rendering bitmap resources. It bridges the launcher's UI with Windows GDI for bitmap display, likely used for splash screens or loading indicators.

## Cross-References
### Incoming
- Not inferable (no callers visible in this file)

### Outgoing
- **Windows GDI**: Directly calls GDI functions (e.g., `CreateDIBitmap`, `StretchBlt`) for bitmap rendering.
- **Windows API**: Uses file I/O (`CreateFile`, `ReadFile`) and window management (`InvalidateRect`, `GetClientRect`).

## Design Patterns
- **Resource Management**: Uses RAII-like patterns for GDI handles (e.g., `DeleteObject` in destructor), though not strictly RAII due to manual cleanup.
- **Facade**: Wraps complex GDI bitmap operations behind a simple `LoadBmp` class interface.
- **Not inferable**: No clear use of other patterns (e.g., no factories, observers, or strategies).

*(Token count: ~200)*
