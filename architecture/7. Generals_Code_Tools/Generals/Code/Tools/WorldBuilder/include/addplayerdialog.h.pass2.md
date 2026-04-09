# Generals/Code/Tools/WorldBuilder/include/addplayerdialog.h - Enhanced Analysis

## Architectural Role
This header defines the UI layer for player addition in WorldBuilder, bridging MFC dialog infrastructure with game-specific side selection logic. It encapsulates the dialog's state and behavior, serving as a thin abstraction over MFC's CDialog.

## Cross-References
### Incoming
- Likely called from `WorldBuilder`'s main window or map editor context menus (not explicitly referenced in header).

### Outgoing
- Uses `GameLogic/SidesList.h` for side enumeration.
- Relies on MFC framework classes (`CDialog`, `CWnd`, etc.).

## Design Patterns
- **MVC (Model-View-Controller)**: The dialog acts as the view/controller, with `m_side` and `m_addedSide` as part of the model.
- **Template Method**: Overrides MFC's virtual methods (`DoDataExchange`, `OnInitDialog`) to customize behavior.
- **Observer**: Event handlers (`OnEditchangeCombo1`) react to UI changes, though the pattern is implicit in MFC's message loop.
