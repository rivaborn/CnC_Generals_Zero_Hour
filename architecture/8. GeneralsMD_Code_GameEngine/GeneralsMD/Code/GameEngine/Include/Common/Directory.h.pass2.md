# GeneralsMD/Code/GameEngine/Include/Common/Directory.h - Enhanced Analysis

## Architectural Role
This header defines the core abstraction for filesystem operations in the SAGE engine, bridging Windows API calls with the engine's internal string and container types. It's a foundational utility for resource loading, modding, and asset management.

## Cross-References
### Incoming
- Likely called by resource managers (e.g., W3D model loader, audio system) and modding infrastructure for directory scanning.
- May be used by the UI system for file dialogs or save/load functionality.

### Outgoing
- Uses `AsciiString` for path handling, indicating tight integration with the engine's string abstraction layer.
- Relies on STL containers (`std::set`) for sorted file/subdirectory storage, suggesting a design preference for ordered traversal.

## Design Patterns
- **Adapter Pattern**: Wraps Windows-specific `WIN32_FIND_DATA` into a cross-platform-friendly `FileInfo` class.
- **Composite Pattern**: `Directory` aggregates `FileInfo` objects into hierarchical sets (`m_files`, `m_subdirs`).
- **Strategy Pattern**: `FileInfoComparator` encapsulates the sorting logic for flexibility (though not dynamically swapped here).
