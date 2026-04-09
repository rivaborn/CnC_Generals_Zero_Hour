# Generals/Code/Tools/WorldBuilder/include/EditAction.h - Enhanced Analysis

## Architectural Role
This header defines the `EditAction` dialog class, a key component of WorldBuilder's script editing UI. It bridges the gap between the game's scripting system and the editor's visual interface, allowing level designers to modify script actions interactively.

## Cross-References
### Incoming
- Likely called by WorldBuilder's main editor UI when script actions need editing
- May be referenced by script management systems in WorldBuilder

### Outgoing
- Interacts with `ScriptAction` class for script data manipulation
- Uses MFC's `CDialog` and `CRichEditCtrl` for UI implementation
- References `SidesList` for faction-related script parameters

## Design Patterns
- **MVC (Model-View-Controller)**: Separates script data (`ScriptAction`) from its presentation in the dialog
- **Observer**: Uses Windows notifications (`OnNotify`) to react to UI changes
- **State Management**: Tracks editing state with `m_updating` and `m_modifiedTextColor` flags

*Not inferable: No clear use of other patterns like Factory or Strategy in this header alone.*
