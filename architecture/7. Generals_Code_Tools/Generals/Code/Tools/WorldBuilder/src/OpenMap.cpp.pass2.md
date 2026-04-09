# Generals/Code/Tools/WorldBuilder/src/OpenMap.cpp - Enhanced Analysis

## Architectural Role
This file implements the map selection UI for WorldBuilder, bridging the tool's UI layer with the filesystem. It handles both system and user map directories, reflecting the engine's dual-path resource loading architecture.

## Cross-References
### Incoming
- Called by WorldBuilder's main UI framework when map opening is initiated
- Uses MFC dialog infrastructure (CDialog, CListBox)

### Outgoing
- Queries `TheGlobalData` for user data paths
- Uses Windows API for filesystem operations (FindFirstFile, etc.)
- Interacts with MFC controls for UI updates

## Design Patterns
- **MVC**: Separates map data (filesystem) from presentation (listbox)
- **Strategy**: Different behavior for system vs user maps via `m_usingSystemDir` flag
- **Observer**: Listbox updates trigger dialog state changes (OK button enablement)

*Not inferable*: No clear use of Factory, Singleton, or Visitor patterns.
