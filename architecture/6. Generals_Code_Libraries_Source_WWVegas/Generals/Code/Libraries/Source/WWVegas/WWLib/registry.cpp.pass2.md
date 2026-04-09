# Generals/Code/Libraries/Source/WWVegas/WWLib/registry.cpp - Enhanced Analysis

## Architectural Role
This file provides a cross-platform abstraction layer for Windows Registry operations, serving as the central point for configuration persistence across the engine. It bridges the OS-specific registry API with the game's internal data types (StringClass, WideStringClass), enabling consistent configuration management for settings, save games, and mod data.

## Cross-References
### Incoming
- `WWDownload/registry.cpp` (uses `RegistryClass` methods for download-related settings)
- Likely other subsystems (e.g., UI, audio, networking) for persistent configuration

### Outgoing
- Directly calls Windows Registry API (`RegCreateKeyEx`, `RegQueryValueEx`, etc.)
- Uses WWLib types (`StringClass`, `WideStringClass`, `DynamicVectorClass`)

## Design Patterns
- **Facade Pattern**: Hides Windows Registry complexity behind a simple interface
- **RAII**: Registry key lifecycle managed via constructor/destructor
- **Type Adapter**: Converts between Windows Registry types (REG_DWORD, REG_SZ) and game types (int, float, bool, string)

*Not inferable*: No clear use of Singleton or Factory patterns.
