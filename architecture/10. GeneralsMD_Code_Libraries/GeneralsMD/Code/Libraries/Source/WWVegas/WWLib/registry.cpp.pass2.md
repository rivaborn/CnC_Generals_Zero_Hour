# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/registry.cpp - Enhanced Analysis

## Architectural Role
This file provides a cross-platform abstraction layer for Windows Registry operations, bridging the engine's configuration system with the OS. It's critical for persistent settings storage (graphics, audio, controls) and mod compatibility, as it handles both direct registry access and INI-based fallbacks.

## Cross-References
### Incoming
- `WWDownload` subsystem uses registry helpers for download manager settings
- Game configuration modules likely call `Get_Int/Set_Int` for user preferences
- Mod loading infrastructure may use `Save_Registry_Tree` for mod metadata

### Outgoing
- Directly calls Windows Registry API (`RegOpenKeyEx`, `RegSetValueEx`)
- Uses `INIClass` for registry serialization
- Depends on `rawfile.h` for file I/O operations

## Design Patterns
- **Facade Pattern**: Hides Windows Registry complexity behind simple methods
- **Resource Management**: RAII for registry key handles (constructor/destructor)
- **Adapter Pattern**: Converts between registry types (REG_DWORD) and C++ types (int, float)

*Not inferable*: No clear use of Singleton or Factory patterns despite global `IsLocked` state.
