# Generals/Code/Tools/WorldBuilder/include/MeshMoldTool.h - Enhanced Analysis

## Architectural Role
This file defines the terrain deformation tool used in WorldBuilder, a level editing utility. It extends the base `Tool` class to provide mesh-based heightmap modifications, integrating with the document-view architecture of the editor.

## Cross-References
### Incoming
- `WorldBuilderDoc` (likely calls `apply()` and mouse event handlers)
- Other `Tool`-derived classes (may reference static methods like `updateMeshLocation()`)

### Outgoing
- `WorldHeightMapEdit` (for heightmap modifications)
- `Tool` base class (inherited interface implementation)
- `WbView` (for view coordinate conversions)

## Design Patterns
- **Command Pattern**: Encapsulates terrain modification operations (e.g., `apply()`) for undo/redo support.
- **Singleton-like Static State**: Uses static members (`m_toolPos`, `m_tracking`) for tool-wide state, though not a pure singleton.
- **Observer Pattern**: Mouse event handlers (`mouseDown/Up/Moved`) suggest interaction with the view system.

*Not inferable*: No clear use of Factory, Strategy, or Visitor patterns.
