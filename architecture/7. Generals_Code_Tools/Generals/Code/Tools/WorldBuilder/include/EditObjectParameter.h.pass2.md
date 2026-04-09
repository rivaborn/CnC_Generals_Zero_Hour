# Generals/Code/Tools/WorldBuilder/include/EditObjectParameter.h - Enhanced Analysis

## Architectural Role
This header defines the UI layer for WorldBuilder's object parameter editor, bridging the MFC dialog framework with the game's scripting and template systems. It encapsulates the parameter editing workflow for map designers.

## Cross-References
### Incoming
- Likely called by WorldBuilder's main editor UI (e.g., when "Edit Parameters" is selected)
- Uses `Parameter` class from `GameLogic/Scripts.h` for parameter storage
- References `ThingTemplate` (game object templates) and `SidesList` (faction management)

### Outgoing
- Interacts with MFC's `CDialog`, `CTreeCtrl`, and DDX/DDV mechanisms
- Manipulates tree view controls for hierarchical parameter display
- Presumably modifies `Parameter` objects when OK is clicked

## Design Patterns
- **MVC (Model-View-Controller)**: Separates parameter data (`Parameter`), tree view UI (`CTreeCtrl`), and dialog logic
- **Composite**: Tree structure (`findOrAdd`) suggests hierarchical object organization
- **Observer**: Dialog reacts to user input (OK/Cancel) to trigger parameter updates

*Not inferable*: Exact parameter modification flow or scripting integration details.
