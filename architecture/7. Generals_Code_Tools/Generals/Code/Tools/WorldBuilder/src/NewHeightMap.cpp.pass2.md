# Generals/Code/Tools/WorldBuilder/src/NewHeightMap.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI dialog for heightmap configuration in WorldBuilder, bridging user input with the terrain generation system. It handles dimension parameters and anchor points, which are critical for map editing workflows.

## Cross-References
### Incoming
- Likely called from WorldBuilder's main UI framework when "New Heightmap" action is triggered
- May be referenced by terrain editing commands that need to show this dialog

### Outgoing
- Calls MFC dialog framework (CDialog, CWnd, CButton)
- Uses WorldBuilder's TNewHeightInfo struct to pass parameters
- Interacts with standard C++ types (Int, Bool) for data handling

## Design Patterns
- **Command Pattern**: Button clicks are handled as commands (OnCommand), delegating to specific handlers (doAnchorButton)
- **MVC (Model-View-Controller)**: Separates heightmap data (TNewHeightInfo) from its presentation (dialog controls)
- **State Pattern**: Anchor point selection modifies the internal state (anchor flags) of TNewHeightInfo

*Not inferable*: No clear use of Factory, Observer, or Strategy patterns in this file.
