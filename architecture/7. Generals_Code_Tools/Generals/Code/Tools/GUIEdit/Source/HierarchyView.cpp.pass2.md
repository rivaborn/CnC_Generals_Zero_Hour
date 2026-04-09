# Generals/Code/Tools/GUIEdit/Source/HierarchyView.cpp - Enhanced Analysis

## Architectural Role
This file implements the visual hierarchy editor for the GUIEdit tool, enabling designers to manipulate window parent-child relationships. It bridges the abstract GameWindow tree structure with a concrete Windows tree view control, handling drag-and-drop operations and maintaining editor state.

## Cross-References
### Incoming
- **GUIEditWindowManager**: Likely instantiates and manages the HierarchyView singleton
- **Properties**: Called when modifying window relationships (e.g., after drag-drop)
- **EditWindow**: Uses hierarchy operations during window editing

### Outgoing
- **GameClient/Gadget.h**: Relies on GameWindow's parent/child methods
- **Windows API**: Directly uses TreeView_* functions and message handling
- **Common/Debug.h**: For assertion and logging

## Design Patterns
- **Singleton**: `TheHierarchyView` provides global access to the hierarchy editor
- **Observer**: Tree view updates trigger window relationship changes (e.g., `moveWindowChildOf`)
- **Mediator**: Coordinates between Windows controls and GameWindow hierarchy

*Not inferable*: Exact drag-and-drop implementation details (e.g., whether using COM or raw Win32).
