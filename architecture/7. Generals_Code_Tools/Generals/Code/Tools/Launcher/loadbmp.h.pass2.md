# Generals/Code/Tools/Launcher/loadbmp.h - Enhanced Analysis

## Architectural Role
This header defines a lightweight utility class for loading and rendering BMP files in Windows GDI, specifically for the game launcher. It bridges the toolchain with Windows-specific graphics primitives, abstracting low-level bitmap handling.

## Cross-References
### Incoming
- Likely called by launcher UI code (e.g., splash screens, loading dialogs) in `Generals/Code/Tools/Launcher/` directory.
- May be referenced by build/test tools that require bitmap display.

### Outgoing
- Uses Windows GDI (`HBITMAP`, `HPALETTE`) and custom types (`bit8` from `wstypes.h`).
- Depends on `winblows.h` (likely a wrapper for Windows API calls).

## Design Patterns
- **RAII (Resource Acquisition Is Initialization)**: Manages Windows resources (bitmaps/palettes) via constructor/destructor.
- **Facade**: Hides Windows GDI complexity behind a simple interface (`init()`/`drawBmp()`).
- **Not inferable**: No clear use of other patterns (e.g., no inheritance, singletons, or observers visible).

*Token count: 198*
