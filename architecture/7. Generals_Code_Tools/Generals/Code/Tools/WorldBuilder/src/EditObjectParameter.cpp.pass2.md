# Generals/Code/Tools/WorldBuilder/src/EditObjectParameter.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI dialog for object parameter editing in WorldBuilder, bridging the gap between the editor's UI layer and the game's object template system. It serves as a concrete example of how the SAGE engine's modding tools interact with core game data structures.

## Cross-References
### Incoming
- Called by WorldBuilder's parameter editing system when object selection is needed
- Likely invoked by the property grid or attribute editor when an object parameter is edited

### Outgoing
- Uses `ThingFactory` to enumerate available object templates
- Calls into `EditParameter` for loading object type lists
- Interacts with MFC's tree view control for UI rendering

## Design Patterns
- **Composite Pattern**: The tree view hierarchy organizes objects by side and editor sorting categories
- **Factory Method**: Relies on `ThingFactory` to create and manage object templates
- **Observer Pattern**: The dialog updates the parameter system when OK is clicked (via `friend_setString`)

*Not inferable*: No clear use of Strategy or Visitor patterns despite hierarchical data organization.
