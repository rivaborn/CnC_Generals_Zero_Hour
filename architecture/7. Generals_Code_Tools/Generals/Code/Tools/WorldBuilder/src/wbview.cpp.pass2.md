# Generals/Code/Tools/WorldBuilder/src/wbview.cpp - Enhanced Analysis

## Architectural Role
This file implements the core view logic for WorldBuilder, bridging MFC's CView with the game's custom tooling system. It handles input routing, object selection, and view state management, acting as the primary interface between the editor's UI and the underlying map data.

## Cross-References
### Incoming
- **Tools**: `WbApp()->getCurTool()->mouseDown/mouseMoved/mouseUp` (tool interaction)
- **Rendering**: `TheTerrainRenderObject->getHeightMapHeight` (terrain queries)
- **Undo System**: `CWorldBuilderDoc::AddAndDoUndoable` (validation fixes)
- **Dialogs**: `CTeamsDialog`, `CPlayerListDlg` (editor UI)

### Outgoing
- **MFC Framework**: `CView` base class, message map handlers
- **Game Data**: `TheSidesList`, `Dict` classes (team/player management)
- **Preferences**: `AfxGetApp()->GetProfileInt/WriteProfileInt` (persistent settings)

## Design Patterns
- **Command Pattern**: Used for undoable actions (e.g., `DictItemUndoable`), decoupling action execution from history tracking.
- **Observer Pattern**: View state changes (e.g., `m_showNames`) trigger invalidations, notifying other views via `WbDoc()->GetActive2DView()`.
- **State Pattern**: `m_pickConstraint` filters object selection, implicitly switching behavior based on editor mode.
