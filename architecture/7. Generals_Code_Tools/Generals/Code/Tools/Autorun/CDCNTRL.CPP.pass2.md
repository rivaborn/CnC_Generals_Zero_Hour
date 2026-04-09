# Generals/Code/Tools/Autorun/CDCNTRL.CPP - Enhanced Analysis

## Architectural Role
This file implements low-level CD/DVD drive control functionality, serving as a platform abstraction layer for media handling operations. It bridges the game's autorun tool with Windows-specific APIs for drive locking, ejection, and volume management.

## Cross-References
### Incoming
- Likely called by autorun initialization code (e.g., CD autorun handler)
- Potentially referenced by installation/updater tools for media verification

### Outgoing
- Directly uses Windows APIs: `DeviceIoControl`, `CreateFile`, `FormatMessage`
- Depends on `WinVersion` class for OS detection
- Uses `Msg()` for error reporting (likely from a shared utility module)

## Design Patterns
- **Facade Pattern**: Wraps complex Windows-specific CD control operations behind a simplified interface
- **Adapter Pattern**: Provides different implementations for Win9x vs. NT/2000 (e.g., `Lock_CD_Drive_95` vs. `Lock_CD_Drive`)
- **Singleton Pattern**: Global `CDControl` instance ensures single point of control for CD operations

*Not inferable*: No clear use of Observer or Strategy patterns in the visible code.
