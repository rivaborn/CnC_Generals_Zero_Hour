# Generals/Code/Tools/WorldBuilder/include/EyedropperTool.h - Enhanced Analysis

## Architectural Role
This file defines a tool class within WorldBuilder's editor framework, specifically for texture selection. It extends the base Tool class, integrating into the editor's command pattern for tool operations.

## Cross-References
### Incoming
- Likely called by WorldBuilder's tool manager when the eyedropper tool is selected
- Mouse event handlers in the editor's view system would invoke mouseDown()

### Outgoing
- Inherits from Tool.h, using its virtual interface
- Interacts with WbView and CWorldBuilderDoc for view and document state
- May use WorldHeightMapEdit for terrain texture application

## Design Patterns
- **Command Pattern**: Implements tool operations as command objects
- **Template Method**: mouseDown() and activate() are virtual hooks for tool behavior
- **Dependency Injection**: Receives view and document objects as parameters

*Not inferable*: No other patterns clearly visible from header alone.
