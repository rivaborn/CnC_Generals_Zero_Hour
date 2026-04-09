# Generals/Code/Tools/WorldBuilder/include/AutoEdgeOutTool.h

## Purpose
Defines the AutoEdgeOutTool class for blending terrain edges in WorldBuilder.

## Responsibilities
- Implements edge-blending functionality for terrain
- Handles mouse input for tool activation
- Manages tool activation/deactivation lifecycle

## Key Types
- AutoEdgeOutTool (Class): Edge-blending tool implementation
- WorldHeightMapEdit (Class): External heightmap editing interface

## Key Functions
### AutoEdgeOutTool()
- Purpose: Default constructor
- Calls: None

### ~AutoEdgeOutTool()
- Purpose: Destructor
- Calls: None

### mouseDown()
- Purpose: Handles mouse click to trigger edge blending
- Calls: Not inferable

### activate()
- Purpose: Activates the tool as current selection
- Calls: Not inferable

## Globals
None

## Dependencies
- Tool.h (base class)
- WorldHeightMapEdit (forward declaration)
- TTrackingMode, CPoint, WbView, CWorldBuilderDoc (external types)
