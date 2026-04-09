# Generals/Code/Tools/WorldBuilder/src/ScriptActionsTrue.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI layer for script action management in WorldBuilder, bridging the MFC-based property page framework with the game's script system. It handles the presentation and manipulation of script actions, acting as a controller between the UI and the underlying `ScriptAction` linked list.

## Cross-References
### Incoming
- Called by MFC framework for property page lifecycle (e.g., `OnInitDialog`, message handlers)
- Likely invoked by `ScriptDialog` or parent property sheet when script editing is initiated

### Outgoing
- Interacts with `ScriptAction` objects (traversal, modification)
- Uses `ScriptDialog` for validation feedback
- Spawns `EditAction` modal dialogs for detailed action editing

## Design Patterns
- **Linked List Traversal**: Manages script actions as a linked list, with manual traversal for selection/movement
- **MVC Separation**: UI state (`m_action`, `m_index`) is decoupled from model (`ScriptAction` objects)
- **Command Pattern**: Action modifications (new/copy/delete/move) are encapsulated as discrete operations

*Not inferable*: No clear use of Observer, Factory, or Strategy patterns in this snippet.
