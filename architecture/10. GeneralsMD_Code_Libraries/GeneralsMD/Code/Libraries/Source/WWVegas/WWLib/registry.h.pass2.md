# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/registry.h - Enhanced Analysis

## Architectural Role
This file provides a cross-platform abstraction layer for Windows registry operations, enabling configuration persistence and game settings management. It bridges the gap between the game's runtime configuration needs and the underlying OS registry API.

## Cross-References
### Incoming
- Game initialization modules (likely in `GeneralsMD/Code/Game/Source/`)
- Save/load systems (e.g., `GeneralsMD/Code/Game/Source/SaveLoad/`)
- UI configuration handlers (e.g., `GeneralsMD/Code/Game/Source/UI/`)

### Outgoing
- Windows registry API (`RegOpenKeyEx`, `RegSetValueEx`, etc.)
- `INIClass` for bulk registry operations (INI file I/O)
- `StringClass` and `WideStringClass` for string handling

## Design Patterns
- **Facade Pattern**: Hides Windows registry complexity behind a simple interface.
- **Singleton-like behavior**: Implicitly managed via static methods (`IsLocked`, bulk operations).
- **Resource Management**: Encapsulates `HKEY` handles with RAII-style construction/destruction.
