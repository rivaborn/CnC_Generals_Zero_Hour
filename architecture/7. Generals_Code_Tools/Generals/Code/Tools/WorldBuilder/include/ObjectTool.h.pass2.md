# Generals/Code/Tools/WorldBuilder/include/ObjectTool.h - Enhanced Analysis

## Architectural Role
This file defines the `ObjectTool` class, a concrete tool implementation in the WorldBuilder editor's tool system. It extends the base `Tool` class to provide terrain edge blending functionality, integrating with the editor's view and document systems.

## Cross-References
### Incoming
- `Generals/Code/Tools/WorldBuilder/src/WorldBuilderView.cpp` (likely calls `activate`, `deactivate`, mouse event handlers)
- Other tool manager classes in WorldBuilder

### Outgoing
- `Tool.h` (base class)
- `WbView` (for view-related operations)
- `CWorldBuilderDoc` (for document modifications)

## Design Patterns
- **Template Method**: Overrides virtual methods from `Tool` to implement specific behavior.
- **Observer**: Reacts to mouse events (down, up, moved) to modify the document state.
- **Strategy**: Encapsulates a specific tool behavior that can be swapped at runtime.

(Not inferable: No clear use of other patterns like Factory, Singleton, or Decorator.)
