# Generals/Code/Tools/Autorun/WinFix.H - Enhanced Analysis

## Architectural Role
This header defines the `WindowsVersionInfo` class, a singleton used throughout the engine to detect and expose Windows OS version information. It serves as a cross-cutting utility for conditional compilation and runtime checks, particularly for Windows 9x vs. NT/2000/XP compatibility layers.

## Cross-References
### Incoming
- Likely called by:
  - `Generals/Code/Tools/Autorun/WinFix.CPP` (implementation)
  - Build system scripts (for version gating)
  - Game initialization code (early OS checks)
  - Registry/INI handling modules (for OS-specific paths)

### Outgoing
- Uses Windows API (`GetVersionEx`, `GetSystemInfo`) - not shown in header
- No other subsystem dependencies (header-only)

## Design Patterns
- **Singleton**: `WinVersion` global instance ensures single OS detection point
- **Facade**: Wraps complex Windows API version detection into simple methods
- **Query Object**: Methods like `Is_Win9x()` provide read-only OS state queries

*Not inferable*: No other patterns evident from header alone.
