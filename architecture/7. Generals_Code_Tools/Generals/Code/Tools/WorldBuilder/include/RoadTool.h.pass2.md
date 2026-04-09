# Generals/Code/Tools/WorldBuilder/include/RoadTool.h - Enhanced Analysis

## Architectural Role
This file defines the `RoadTool` class, a specialized tool within WorldBuilder's editing framework. It extends the base `Tool` class to handle road segment placement, integrating with the heightmap system and UI event handling.

## Cross-References
### Incoming
- WorldBuilder's tool management system (likely `ToolManager`) instantiates and uses `RoadTool`.
- UI event handlers (mouse input) dispatch to `RoadTool`'s virtual methods.

### Outgoing
- Calls `WorldHeightMapEdit` for terrain modification.
- Uses `MapObject` for road segment creation.
- Relies on `Coord3D` for spatial calculations.

## Design Patterns
- **Template Method**: Overrides `Tool` base class methods (`mouseDown`, `mouseMoved`, etc.) for road-specific behavior.
- **Strategy**: Encapsulates road placement logic as a reusable tool component.
- **Observer**: Reacts to mouse events (implicit UI event handling pattern).
