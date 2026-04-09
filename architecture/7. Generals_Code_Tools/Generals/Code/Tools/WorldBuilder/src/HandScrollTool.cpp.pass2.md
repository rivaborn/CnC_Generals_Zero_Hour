# Generals/Code/Tools/WorldBuilder/src/HandScrollTool.cpp - Enhanced Analysis

## Architectural Role
This file implements the hand scrolling tool for WorldBuilder, a critical UI component that enables camera manipulation in the map editor. It bridges user input (mouse events) with the view system, allowing designers to navigate the 3D workspace efficiently.

## Cross-References
### Incoming
- Called by the WorldBuilder tool system when the hand scroll tool is active
- Mouse event handlers are invoked by the MFC-based view system

### Outgoing
- Calls into `WbView` for camera operations (scrolling, rotation, coordinate conversion)
- Interacts with `WbApp` for tool switching
- Uses `::GetTickCount()` for timing (Windows API)

## Design Patterns
- **Command Pattern**: Encapsulates camera manipulation as a tool that can be activated/deactivated
- **State Pattern**: Tracks scrolling state (`m_scrolling`) to differentiate between selection and movement
- **Strategy Pattern**: Implements specific mouse handling logic as part of a larger tool framework

*Not inferable*: No explicit use of Observer or Factory patterns visible in this file.
