# Generals/Code/Tools/GUIEdit/Include/WinMain.h - Enhanced Analysis

## Architectural Role
This header serves as the entry point for the GUIEdit tool's Win32 application layer, bridging the tool with the underlying Windows API and input systems. It provides global handles and interfaces critical for the tool's window management and input processing.

## Cross-References
### Incoming
- Likely called by `GUIEdit.cpp` (main tool executable) and other tool-specific modules needing window/instance handles
- Potentially referenced by input handling modules (e.g., mouse/keyboard processors)

### Outgoing
- Depends on `Win32Device/GameClient/Win32Mouse.h` for mouse input abstraction
- Uses standard Windows API (`<windows.h>`) for core application services

## Design Patterns
- **Global Access Pattern**: Exposes critical application resources (window handles, mouse interface) via extern globals for tool-wide access
- **Dependency Injection**: `TheWin32Mouse` pointer suggests a pluggable input system design
- **Timer-Based Event Handling**: `TIMER_EDIT_WINDOW_PULSE` constant implies a periodic update mechanism (likely for UI refreshes)

*Not inferable*: No clear evidence of other patterns from this header alone.
