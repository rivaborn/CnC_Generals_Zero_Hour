# Generals/Code/Tools/WorldBuilder/include/NewHeightMap.h - Enhanced Analysis

## Architectural Role
This header defines the UI layer for height map configuration in WorldBuilder, bridging the gap between the editor's terrain manipulation tools and the underlying height map data structures. It encapsulates the dialog logic for user input validation and anchor point management during terrain resizing operations.

## Cross-References
### Incoming
- Likely called by WorldBuilder's terrain editing tools (e.g., terrain resize operations)
- May be referenced by other dialog classes handling map properties

### Outgoing
- Uses MFC's dialog framework (`CDialog`, `CDataExchange`)
- Relies on `TNewHeightInfo` struct for data exchange with terrain systems

## Design Patterns
- **MVC (Model-View-Controller)**: The dialog acts as the view/controller for the height map model (`TNewHeightInfo`)
- **Data Transfer Object**: `TNewHeightInfo` serves as a DTO between UI and terrain systems
- **Command Pattern**: `OnCommand()` suggests handling of UI events as commands (though implementation details are missing)

*Not inferable*: No clear use of Factory, Observer, or Strategy patterns from header alone.
