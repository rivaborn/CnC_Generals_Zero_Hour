# Generals/Code/Tools/WorldBuilder/include/FenceTool.h - Enhanced Analysis

## Architectural Role
This file defines the `FenceTool` class, a specialized tool in WorldBuilder for placing and managing fence-like objects (e.g., barriers, walls) on the map. It extends the base `Tool` class, integrating with WorldBuilder's editing pipeline for terrain and object manipulation.

## Cross-References
### Incoming
- **WorldBuilder UI**: Calls `activate()`/`deactivate()` when the tool is selected/deselected.
- **Input System**: Invokes `mouseDown()`, `mouseUp()`, and `mouseMoved()` for real-time interaction.
- **Map Editor Core**: Likely uses `updateMapObjectList()` during object placement validation.

### Outgoing
- **Tool Base Class**: Inherits and overrides virtual methods from `Tool`.
- **WorldBuilder Document**: Accesses `CWorldBuilderDoc` for map state (e.g., heightmap, object layers).
- **WbView**: Uses `WbView` for view transformation and coordinate mapping.

## Design Patterns
- **Template Method**: Overrides `Tool` virtual methods (`mouseDown`, `mouseUp`, etc.) to define fence-specific behavior.
- **State Pattern**: Tracks tool state (e.g., `m_downPt2d`, `m_downPt3d`) to manage interaction phases (drag, release).
- **Dependency Injection**: Receives `MapObject` and `WbView` instances via method parameters, decoupling from concrete implementations.
