# Generals/Code/Tools/WorldBuilder/include/BlendEdgeTool.h

## Purpose
Defines the BlendEdgeTool class for texture tiling operations in WorldBuilder.

## Responsibilities
- Implements texture blending at map edges
- Handles mouse input for tool activation
- Manages coordinate tracking during tool use

## Key Types
- BlendEdgeTool (Class): Texture blending tool for WorldBuilder
- WorldHeightMapEdit (Class): External dependency for heightmap editing

## Key Functions
### BlendEdgeTool()
- Purpose: Default constructor for BlendEdgeTool
- Calls: None

### ~BlendEdgeTool()
- Purpose: Destructor for BlendEdgeTool
- Calls: None

### mouseDown()
- Purpose: Handles mouse down event for tool activation
- Calls: None (implementation not shown)

### mouseUp()
- Purpose: Handles mouse up event for tool completion
- Calls: None (implementation not shown)

## Globals
- None

## Dependencies
- Tool.h (base class)
- WorldHeightMapEdit (forward declaration)
- CPoint, WbView, CWorldBuilderDoc (external types)
