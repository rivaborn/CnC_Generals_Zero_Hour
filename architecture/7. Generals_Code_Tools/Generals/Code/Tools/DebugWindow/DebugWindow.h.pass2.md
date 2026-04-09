# Generals/Code/Tools/DebugWindow/DebugWindow.h - Enhanced Analysis

## Architectural Role
This header defines the core MFC-based application class for the debug window tool, serving as the entry point for the DLL. It bridges the debug tool's UI with the game engine's debugging infrastructure, allowing runtime inspection/modification of game state.

## Cross-References
### Incoming
- Likely called by the game's main executable or other tools when launching the debug window.
- `DebugWindowDialog` implementation (not shown) would include this header.

### Outgoing
- Uses MFC framework (`CWinApp`) for Windows application structure.
- Relies on `DebugWindowExport.h` for DLL export macros, indicating this is part of a shared library.

## Design Patterns
- **Singleton-like behavior**: The app class manages a single dialog instance via `GetDialogWindow`/`SetDialogWindow`, suggesting a centralized debug interface.
- **MFC message pump**: Uses `DECLARE_MESSAGE_MAP()` for Windows message handling, typical of 90s/early 2000s Windows apps.
- **Forward declaration**: Uses `DebugWindowDialog` forward declaration to decouple from dialog implementation.
