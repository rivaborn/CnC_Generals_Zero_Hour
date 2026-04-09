# Generals/Code/Tools/WorldBuilder/include/SaveMap.h - Enhanced Analysis

## Architectural Role
This header defines the UI layer for map save/load operations in WorldBuilder, bridging the editor's core functionality with MFC-based dialogs. It encapsulates the presentation logic for map I/O, separating it from the underlying map serialization systems.

## Cross-References
### Incoming
- Likely called by WorldBuilder's main editor window (e.g., `CWorldBuilderView`) when "Save Map" is invoked
- May be referenced by map management dialogs or the main menu system

### Outgoing
- Interacts with MFC framework classes (`CDialog`, `CDataExchange`)
- Probably calls into `CFileDialog` for browse functionality
- Likely references map path utilities (e.g., `GetSystemMapsPath()`)

## Design Patterns
- **MVC (Model-View-Controller)**: The `SaveMap` class acts as the View/Controller for map save operations, with the actual map data being the Model
- **Strategy Pattern**: Directory switching (`OnSystemMaps`/`OnUserMaps`) suggests a strategy for map location handling
- **Observer Pattern**: Selection change handler (`OnSelchangeSaveList`) implies event-driven UI updates

*Not inferable*: Exact serialization mechanisms or map format handling.
