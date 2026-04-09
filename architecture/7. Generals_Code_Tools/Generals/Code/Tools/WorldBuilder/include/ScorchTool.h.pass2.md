# Generals/Code/Tools/WorldBuilder/include/ScorchTool.h - Enhanced Analysis

## Architectural Role
This file defines the ScorchTool class, part of WorldBuilder's tool system. It extends the base Tool class to provide scorch effect placement functionality in the map editor, bridging user input handling with map object manipulation.

## Cross-References
### Incoming
- WorldBuilder's tool management system (likely ToolManager) instantiates and uses ScorchTool
- WbView handles view-related callbacks (mouseDown/mouseMoved/mouseUp)
- CWorldBuilderDoc manages document state for scorch operations

### Outgoing
- Calls into MapObject for scorch object selection (pickScorch)
- Likely interacts with WorldHeightMapEdit for terrain modifications
- Uses base Tool class methods for tool lifecycle management

## Design Patterns
- **Template Method**: Overrides virtual methods from Tool base class (mouseDown/Up/Moved/activate/deactivate)
- **Command**: Encapsulates scorch operation as a tool action triggered by user input
- **Observer**: Reacts to mouse events from WbView (event-driven design)
