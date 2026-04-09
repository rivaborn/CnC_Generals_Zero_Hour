# Generals/Code/Tools/WorldBuilder/include/teamsdialog.h - Enhanced Analysis

## Architectural Role
This header defines the UI layer for team management in WorldBuilder, bridging the MFC dialog framework with the game's team logic (SidesList). It encapsulates team configuration operations while delegating core team data handling to the GameLogic subsystem.

## Cross-References
### Incoming
- Likely called from WorldBuilder's main window or map editor context menus (not explicitly shown in header)
- Uses MFC's CDialog base class and message handlers

### Outgoing
- Depends on `GameLogic/SidesList.h` for team data structure
- Interacts with UI controls (list boxes, buttons) via MFC mechanisms

## Design Patterns
- **Observer Pattern**: Dialog updates UI based on team changes (via `updateUI` and `UpdateTeamsList`)
- **Command Pattern**: Dialog methods like `OnNewteam()`/`OnDeleteteam()` encapsulate team operations
- **State Pattern**: Rebuild flags (`REBUILD_TEAMS`, etc.) manage UI synchronization state

*Not inferable*: Exact relationship with networking or rendering subsystems.
