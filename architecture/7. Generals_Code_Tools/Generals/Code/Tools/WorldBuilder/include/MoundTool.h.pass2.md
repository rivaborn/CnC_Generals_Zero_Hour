# Generals/Code/Tools/WorldBuilder/include/MoundTool.h - Enhanced Analysis

## Architectural Role
This file defines terrain editing tools within WorldBuilder, extending the base `Tool` class to provide heightmap manipulation capabilities. It bridges the UI input layer with the underlying heightmap data structure, enabling real-time terrain sculpting.

## Cross-References
### Incoming
- **WorldBuilder UI**: Calls `mouseDown`, `mouseUp`, `mouseMoved`, and `activate` for tool interaction.
- **Tool Manager**: Likely instantiates `MoundTool` and `DigTool` as active tools.

### Outgoing
- **WorldHeightMapEdit**: Uses `m_htMapEditCopy` and `m_htMapSaveCopy` for heightmap modifications.
- **Tool.h**: Inherits core tool functionality (e.g., activation lifecycle).

## Design Patterns
- **Template Method**: Overrides `mouseDown`/`mouseUp`/`mouseMoved` to define terrain-specific behavior while delegating UI handling to the base `Tool` class.
- **State Pattern**: `m_raising` flag toggles between mounding/digging modes, altering tool behavior dynamically.
- **Singleton-like Globals**: Static `m_moundHeight`, `m_brushWidth`, and `m_brushFeather` ensure tool parameters persist across instances.
