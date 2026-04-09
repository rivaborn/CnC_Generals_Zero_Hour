# Generals/Code/Tools/WorldBuilder/include/ScriptActionsTrue.h - Enhanced Analysis

## Architectural Role
This header defines the UI layer for script action management in WorldBuilder, bridging the gap between the script system and the MFC-based property page framework. It encapsulates the dialog logic for editing, reordering, and manipulating script actions within the editor toolchain.

## Cross-References
### Incoming
- Likely called by the main WorldBuilder property sheet framework (e.g., `CPropertySheet` derivatives)
- May be referenced by script editing workflows in other WorldBuilder modules

### Outgoing
- Interacts with `Script` and `ScriptAction` classes (script system)
- Uses MFC's `CPropertyPage` and `CDataExchange` for UI management
- Potentially references `SidesList` for side-specific script actions

## Design Patterns
- **MVC (Model-View-Controller)**: Separates script data (`Script`/`ScriptAction`) from UI presentation (`ScriptActionsTrue`)
- **Observer**: UI state updates (e.g., `enableUI`) react to selection changes (`OnSelchangeActionList`)
- **Command Pattern**: Action manipulation methods (`OnNew`, `OnDelete`) encapsulate operations as discrete commands

*Not inferable*: Exact relationships with other WorldBuilder modules (e.g., undo/redo system) remain unclear.
