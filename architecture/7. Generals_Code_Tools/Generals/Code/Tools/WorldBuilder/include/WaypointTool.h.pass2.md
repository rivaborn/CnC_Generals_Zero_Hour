# Generals/Code/Tools/WorldBuilder/include/WaypointTool.h - Enhanced Analysis

## Architectural Role
This file defines the WaypointTool class, which is part of WorldBuilder's tool system. It handles waypoint manipulation, bridging the gap between user input and the map's waypoint system, which is critical for mission design and AI pathfinding.

## Cross-References
### Incoming
- Likely called by WorldBuilder's tool manager (e.g., `ToolManager`) to handle waypoint operations.
- May be referenced by `WbView` for view-specific waypoint rendering or interaction.

### Outgoing
- Calls into `MapObject` for waypoint picking logic.
- Interacts with `WorldHeightMapEdit` for terrain-aware waypoint placement (inferred from context).

## Design Patterns
- **Command Pattern**: Encapsulates waypoint operations as methods (e.g., `mouseDown`, `mouseUp`) to decouple tool behavior from the tool manager.
- **Singleton-like State**: Uses static `m_isActive` to track tool activation state, though not a true singleton.
- **Observer Pattern**: Reacts to mouse events (down/moved/up) to modify waypoint state, typical of tool systems.

*Not inferable*: No clear use of Factory, Strategy, or Visitor patterns.
